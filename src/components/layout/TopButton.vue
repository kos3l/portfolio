<template>
  <button id="totop" v-on:click="toTop"><p> TO THE TOP </p></button> 
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
    padding: 0;
}
#top p{
    margin: 0;
}

#top:hover{
    border-top: 2px solid black;
    background-color:black ;
    color: white;
    
}
#top:hover p{

    color: white;
    
    
}
@media screen and (max-width:600px) {
    #totop p{
        font-size: 3vh;
    }
    #top:hover{
    border-top: 2px solid black;
    background-color:white ;
    color: black;
    
    }
    #top:hover p{

        color: black;
        
        
    }
}
</style>