<template>
    <v-col id="display">
            <v-col id="image-wrap">
                <img :src="photo.src" class="picture">
            </v-col>
            <v-col id="title">
                <p>{{ photo.title }}</p>
            </v-col>
    </v-col>
</template>

<script>
export default {
    name: 'ArticleImage',
    props:['photo']

}
</script>

<style>
#display{
    padding: 0;
}
#image-wrap{
    padding: 0;
    border-top: 2px solid black;
    height: 40vh;
}
#title{
    border-top: 2px solid black;
    font-weight: 300;
    letter-spacing: 0.1rem;
    font-size: 1.5vw;
    display: flex;
    align-items: center;
    justify-content: center;
}
#title p {
    margin: 0;
}
.picture{
    
    width: 100%;
    height: 100%;
}
</style>