<template>
        <div id="slides-container">
            <v-col id="display-design">
                    <v-col id="image-wrap-design">
                        <img :src="design.src" class="picture-design">
                    </v-col>
            </v-col>
        </div>
</template>

<script>
export default {
    name:'Design',
    props: ['design']

}
</script>

<style>
#display-design{
    padding: 0;
    margin: 0;
}
#image-wrap-design{

    border-top: 2px solid black;
    height: auto;
    overflow: hidden;
}
.picture-design{

    object-fit: cover;
    width: 100%;
    height: 100%;
    border: 2px solid black;
    
}
.night #slides-container {
    background-color: black;
    border-top: 2px solid white;

}

@media screen and (max-width:600px) {
    #image-wrap-design{
        border-top: 2px solid black;
        border-left: 2px solid black;
        height: auto;
        overflow: hidden;
    }
}
</style>