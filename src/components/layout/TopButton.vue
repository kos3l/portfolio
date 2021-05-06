<template>
  <button id="top" v-on:click="toTop"><p> TO THE TOP </p></button> 
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
    border-top: 1px solid black;
    height: 10vh;
    width: 100%;
    display: flex;
    justify-content: center;
    padding: 0;
    font-weight: 300;
    letter-spacing: 0.1rem;
    font-size: 2vw;
    padding: 0;
    display: flex;
    align-items: center;
}
#top p{
    margin: 0;
    

}

#top:hover{

    background-color:black ;
}
#top:hover p{
    color: white;
}
.night #top{
    border-top: 2px solid white;
}
.night #top:hover{
    background-color:white ;
}
.night #top:hover p{
    color: black;
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