<template>
    <div class="mainWrapper">
        <div class="headerWrapper">
            <div class="headerLogo"><span>O</span>ptical <span>Store</span></div>
            <div class="headerText">Home</div>
            <div class="headerText">Shop</div>
            <div class="headerText">Featured</div>
            <div class="headerText">Recomended</div>
        </div>
        <filter-component
        class="filterComponent"
        ></filter-component>
    </div>
</template>

<script>
import filterComponentVue from './filterComponent.vue'
export default {
    components: {
        filterComponent: filterComponentVue
    }
}
</script>

<style scoped>
.mainWrapper {
        display: flex;
        justify-content: space-around;
}
.headerWrapper {
    display: flex;
    width: 100%;
    height: 60px;
    justify-content: start;
    align-items: center;
}
.headerLogo {
    font-size: 30px;
    margin-bottom: 8px;
}
.headerLogo span:nth-child(1) {
    color: red;
}
.headerLogo span:nth-child(2) {
    color: gray;
    font-size: 23px;
}
.headerText {
    margin-left: 40px;
    font-size: 17px;

}

</style>