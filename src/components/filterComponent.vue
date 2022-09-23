<template>
  <div class="inputWrapper">
    <input class="filterInput" type="text" placeholder="Enter product name">
    <div class="searchButton">Search</div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.inputWrapper {
    display: flex;
    align-items: center;
    position: relative;
    right: -60px;
}
.filterInput {
    width: 350px;
    height: 25px;
}
.searchButton {
    position: relative;
    left: -65px;
    cursor: pointer;
    background-color: gray;
    padding: 5px 10px 6px 12px;
}
</style>