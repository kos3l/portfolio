<template>
  <v-col id="banner" lg="12" md="12" sm="12" class="d-none d-sm-flex" >
   </v-col>
</template>

<script>


export default {
    name: 'Banner',

}
</script>

<style>
    #banner{
    height: 156px;
    border-bottom: 2px solid black;
    background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(151,234,210) 90%);
    
    }
    .animation{
    width: 50px;
    height: 50px;
    background-color: blue;
}


    @media screen and (min-width:1540px) {

    #banner{
        height: 245px;

    }
    }
</style>