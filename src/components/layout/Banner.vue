<template>
    <v-col id="banner" lg="12" md="12" sm="12" class="d-none d-sm-flex" :class="(mode === 'day') ? 'day' : 'night' ">
        <p id="homepage-1" > 
            <span>{{ one }}</span>
            <span>{{ two }}</span>
            <span>{{ three }}</span>
            <span>{{ four }}</span>
            <span>{{ five }}</span>
            <span>{{ six }}</span>
            <span>{{ seven }}</span>
            <span>{{ eight }}</span>
        </p>
    </v-col>
</template>

<script>


export default {
    name: 'Banner',
    props: ['one', 'two', 'three', 'four', 'five', 'six', 'seven', 'eight', 'mode']
    
}



</script>

<style>


    #banner{
    height: 156px;
    background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(60,213,183) 90%);
    margin: 0;
    padding: 0;
    width: 100%;
    
    }
    #homepage-1{
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 12vw;
        letter-spacing: 1.5vw;
        font-weight: 900;
        color: white;
        -webkit-text-stroke-width: 3px;
        -webkit-text-stroke-color: #3CD5B7;
        height: 100%;
        padding: 1vh 3vw 1vh 3.5vw;
        overflow: hidden;
        width: 100%;
    }
     p span {
        transition: color 2s;
        color: white;
    }

    p span:hover {
    color:  #3CD5B7;
    transition: color 0s;
    }
    


.night #banner {
    background: linear-gradient(90deg, rgba(0,0,0,1) 0%, rgba(255,255,255) 90%);
}

.night #banner #homepage-1{
        color: black;
        -webkit-text-stroke-width: 3px;
        -webkit-text-stroke-color: white;

    }
.night #banner  p span {
        transition: color 2s;
        color: black;
    }
.night #banner p span:hover {
    color:  white;
    transition: color 0s;
    }


    @media screen and (min-width:1540px) {

    #banner{
        height: 245px;

    }}
    @media screen and (max-width:900px) {

    #homepage-1{
        display: none;
    }
    }
</style>