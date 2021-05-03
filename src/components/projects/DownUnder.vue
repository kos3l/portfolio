<template>
        <div id="slides-container">
            <v-col id="article-d">
                    <div id="wrapper">
                        <p>{{ downunder.description }}</p>
                    </div>
                    
            </v-col>
            <v-col id="display">
                    <v-col id="image-wrap">
                        <img :src="downunder.src" class="picture">
                    </v-col>
                    <v-col id="title">
                        <p> PREVIEW </p>
                    </v-col>
            </v-col>
        </div>
</template>

<script>
export default {
    name:'DownUnder',
    props: ['downunder']

}
</script>

<style>
#article-d{
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

#article-d h1{
    font-weight: 900;
    color: #C4C4C4;
    padding-bottom: 2vh;
}
#article-d p{
    font-weight: 300;
    letter-spacing: 0.1rem;
    font-size: 1vw;

}
@media screen and (max-width:600px) {
    #article-d p{
    font-size: 3.7vw;

    }
    #article-d{
        padding: 10vw;
        border-left: 2px solid black;

    }
    #display{
        border-left: 2px solid black;
    }
    #title{
        font-size: 6vw;
    }
}
</style>