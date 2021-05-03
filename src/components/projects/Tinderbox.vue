<template>
        <div id="slides-container">
            <v-col id="article-t">
                    <div id="wrapper">
                        <p>{{ tinderbox.description }}</p>
                    </div>
                    
            </v-col>
            <v-col id="display">
                    <v-col id="image-wrap">
                        <img :src="tinderbox.src" class="picture">
                    </v-col>
                    <v-col id="title">
                        <p> PREVIEW</p>
                    </v-col>
            </v-col>
        </div>
</template>

<script>
export default {
    name:'Tinderbox',
    props: ['tinderbox']

}
</script>

<style>
#article-t{
    padding: 6vw;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    border-top: 2px solid black;
    height: 50vh;
    width: 100%;
    background-color: white;
}

#article-t h1{
    font-weight: 900;
    color: #C4C4C4;
    padding-bottom: 2vh;
}
#article-t p{
    font-weight: 300;
    letter-spacing: 0.1rem;
    font-size: 1vw;

}
@media screen and (max-width:600px) {
  #article-t p{

    font-size: 3.7vw;

}
#article-t{

    border-left: 2px solid black;
    padding: 10vw;

}
#display{
    border-left: 2px solid black;
}
#title{
    font-size: 6vw;
}
}
</style>