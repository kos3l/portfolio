<template>
        <div id="slides-container">
            <v-col id="article">
                    <div id="wrapper">
                        <h1>{{ article.head }}</h1>
                        <p>{{ article.body }}</p>
                    </div>
                    
            </v-col>
            <v-col id="display">
                    <v-col id="image-wrap">
                        <img :src="article.src" class="picture">
                    </v-col>
                    <v-col id="title">
                        <p>{{ article.title}}</p>
                    </v-col>
            </v-col>
        </div>
</template>

<script>
export default {
   name: 'ArticleMe',
    props:['article']

}
</script>

<style>
#slides-container{
    width: 100%;
    height: auto;
}
#display{
    padding: 0;
}
#image-wrap{
    padding: 0;
    border-top: 2px solid black;
    height: 45vh;
    overflow: hidden;
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
    object-fit: cover;
    width: 100%;
    height: 100%;
    overflow: hidden;
    
}
#article{
    padding: 6vw;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    border-top: 2px solid black;
    height: 55vh;
    width: 100%;
    background-color: white;
}

#article h1{
    font-weight: 900;
    color: #C4C4C4;
    padding-bottom: 2vh;
}
#article p{
    font-weight: 300;
    letter-spacing: 0.1rem;
    font-size: 1vw;

}

@media screen and (max-width:1263px) {
    #article h1{
        font-size: 3vh;
    }
    #article p{
        font-size: 1.5vh;
    }

}
@media screen and (max-width:600px) {
    #article {
        padding: 10vw;
        border-left: 2px solid black;
    }

}
</style>