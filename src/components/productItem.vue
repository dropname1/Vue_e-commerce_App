<template>
    <div class="mainWrapper">
        <div class="imageWrapper">
            <img class="image" :src="product.image" alt="">
        </div>
        <h3 class="title">{{product.title}}</h3>
        <h3 class="price">price: {{product.price}}</h3>
            <!-- <button class="button" @click="showP">Show Details</button> -->
        <p class="description" v-if="show">{{product.description}}</p>
    </div>
</template>

<script>
export default {
data () {
    return {
        show: false
    }
},
props: [
    'product'
]
}
</script>

<style scoped>
* {
    margin: 0;
}
.mainWrapper {
    display: flex;
    flex-direction: column;
    width: 220px;
    height: 400px;
    border: 1px solid gray;
    background-color: rgb(238, 227, 227);
    justify-content: space-around;

}
.imageWrapper {
    width: 220px;
    display: flex;
    justify-content: center;

}
.image {
    width: 180px;
}
.title {
    margin-bottom: 10px;  
    max-width: 220px;  
}
.price {
    margin-bottom: 10px;
}
.button {
    width: fit-content;
    padding: 5px 10px;
    margin: 0 auto;
    margin-bottom: 10px;
}


</style>