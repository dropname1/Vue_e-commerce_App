<template>
  <div class="mainWrapper">
    <header-component></header-component>
    <product-list></product-list>
  </div>
</template>

<script>
import headerComponentVue from './headerComponent.vue'
import productListVue from './productList.vue'
export default {
  data () {
    return {

    }
  },
  components: {
    headerComponent: headerComponentVue,
    productList:productListVue
  },
  
}
</script>

<style scoped>
.mainWrapper {
    text-align: center;
    width: 90%;
    margin: 0 auto;
}

</style>