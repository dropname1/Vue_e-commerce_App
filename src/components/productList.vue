<template>
    <div v-if="productsArray == false">
        <h2>Loading</h2>
        <div class="lds-circle"><div></div></div>
    </div>
    <div v-else class="mainWrapper">
        <div class="productItemWrapper" v-for="item in productsArray" :key="item">
            <product-item
            :product="item"
            ></product-item>
        </div>
    </div>
</template>

<script>
import productItemVue from './productItem.vue'
export default {

data () {
    return {
        productsUrl: 'https://fakestoreapi.com/products?limit=13',
        productsArray: []
    }
},
components: {
    productItem: productItemVue
},
async mounted () {
    const response = await fetch(this.productsUrl)
    const result = await response.json()
    this.productsArray.push(...result)
    this.productsArray.splice(4,4)
    this.productsArray.splice(7,1)
}
}
</script>

<style scoped>
 .mainWrapper {
    margin-left: 0px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
.lds-circle {
  display: inline-block;
  transform: translateZ(1px);
}
.lds-circle > div {
  display: inline-block;
  width: 64px;
  height: 64px;
  margin: 8px;
  border-radius: 50%;
  background: rgb(99, 192, 255);
  animation: lds-circle 2.4s cubic-bezier(0, 0.2, 0.8, 1) infinite;
}
@keyframes lds-circle {
  0%, 100% {
    animation-timing-function: cubic-bezier(0.5, 0, 1, 0.5);
  }
  0% {
    transform: rotateY(0deg);
  }
  50% {
    transform: rotateY(400deg);
    animation-timing-function: cubic-bezier(0, 0.5, 0.5, 1);
  }
  100% {
    transform: rotateY(800deg);
  }
}


</style>