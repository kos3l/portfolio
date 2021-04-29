<template>
  <div class="About">
    <div id="bg">
      <v-row id="main-row">
        
        <v-col lg="2">
        </v-col>

        <v-col lg="8" id="middle">
          <Banner />
          <ArticleImage v-for="photo in photos" :key="photo.title" :photo="photo"/>

          <v-col id="article">
            <v-col id="text">
            </v-col>
          </v-col>
          
        </v-col>

        <v-col lg="2">
        </v-col>
      </v-row>
    </div>
   
  </div>
</template>

<script>
import Banner from '/src/components/Banner'
import ArticleImage from '/src/components/ArticleImage'
export default {
   name: 'About',
  components: {
    Banner,
    ArticleImage

  },
  data() {
        return {
            photos: [
        { 
          title: "THAT'S ME RIGHT THERE",
          src: require('/src/assets/janakrzesle.jpg'),
          id: 1
        },
        { 
          title: 'COMMISSION',
          src: require('/src/assets/commissions.jpg'),
          id: 2
        },
        { 
          title: 'MY STOP MOTION CLASSES',
          src: require('/src/assets/tinder.png'),
          id: 3
        },
        { 
          title: 'MY FAVOURITE ARTISTS',
          src: require('/src/assets/ilustrejszynFinished.png'),
          id: 4
        },
        { 
          title: 'MY FAVOURITE PAINTINGS',
          src: require('/src/assets/ilustrejszynFinished.png'),
          id: 5
        },
      ]
        }
    }

}
</script>

<style>

#bg{
  width: 100%;
  height: 300vh;
  background-color: grey;
}
#main-row {
  height: 100vh;
  width: 100%;
  margin: 0;
}

#middle{
  background-color: white;
  padding: 0;
  border: 2px solid black;
  border-top: 0;

}

</style>
