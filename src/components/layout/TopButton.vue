<template>
  <button id="totop" v-on:click="toTop"  > TO THE TOP</button> 
</template>

<script>
export default {
    name:'TopButton',
    methods: {
        toTop() {
        this.$vuetify.goTo(0)
        }},
}
</script>

<style>
#top{
    border-top: 2px solid black;
    height: 10vh;
    width: 100%;
    display: flex;
    justify-content: center;
}
</style>