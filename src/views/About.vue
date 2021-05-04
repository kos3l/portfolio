<template>
  <div class="About">
    <div id="bg">
      <v-row id="main-row">
        
        <v-col lg="1" md="1" sm="0" id="column" >
        </v-col>

        <v-col lg="10" md="10" sm="12" id="middle">
          <Banner one="K" two="O" three="S" four="3" five="E" six="L"/>
          <ArticleMe v-for="article in articles" :article="article" :key="article.id" />
          
        </v-col>

        <v-col lg="1" md="1" sm="0" id="column" >
        </v-col>
      </v-row>
    </div>
   
  </div>
</template>

<script>
import Banner from '/src/components/layout/Banner'
import ArticleMe from '/src/components/ArticleMe'

export default {
   name: 'About',
  components: {
    Banner,
    ArticleMe,
  },
  data() {
        return {
          articles: [
            {
              title: "THAT'S ME RIGHT THERE",
              src: require('/src/assets/janakrzesle.jpg'),
              head: "INTRODUCTION",
              body: 'My name is Karolina Kosinska and I’m 20 year old Multimedia design student, based in Esbjerg, Denmark. I chose this education on Business Academy Southwest, since I have a wide range of interests. My first passion was drawing which with time evolved to be graphic design. While growing up I became drawn towards 2D and 3D animation, and languages. Front end web development allows me to be creative and solve problems therefore, working in this field is my main goal as it’s a point where all my passions meet.',
              id: 1
            },
            { 
              title: 'COMMISSION',
              src: require('/src/assets/commissions.jpg'),
              head: 'WORK EXPERIENCE',
              body: 'I have been doing freelance work up to this point. My main commissions were illustrations or icon designs. During my AP degree education I was working on a project called “Tinderbox” for 7-kanten so I also have experience with clients.',
              id: 2

            },
            { 
              title: 'MY STOP MOTION CLASSES',
              src: require('/src/assets/tinder.png'),
              head: 'MY ROOTS',
              body: "I was born and raised in a small town called Brzeg Dolny in Poland. It may seem like a boring place, but it offered me many opportunities to be creative. In primary school I was a part of my town’s stop motion animation course where we created our own movies from scratch. Growing up in a country of contrasts, rich history, many problems and blossoming culture made me who I am now. It inspired me greatly and influenced to be always wondering how could we solve existing problems surrounding us. I always stay realistic and have a back up plan in case something goes wrong. ",
              id: 3

            },
            { 
              title: 'MY FAVOURITE ARTISTS',
              src: require('/src/assets/ilustrejszynFinished.png'),
              head: 'MINDSET',
              body: "In my opinion, there is nothing a person can’t learn. Given enough practice, energy and passion one can become good at any given field. I proved this to myself many times and I want to carry on with this notion further in my life. When working with people, my rule number one is to avoid conflicts. I’m willing to work hard in order to find the best compromise. I’m a rather cheerful and calm person and I love to joke around with colleagues.",
              id: 4
              

            }
          ]
          }}} 
</script>

<style>

#bg{
  width: 100%;
  height: auto;
  background-color: grey;
}
#main-row {
  height: auto;
  width: 100%;
  margin: 0;
}

#middle{
  background-color: white;
  padding: 0;
  border: 2px solid black;
  border-bottom: 0;
  border-top: 0;

}

@media screen and (max-width:900px) {
  #column{
    display: none;
  }
  #middle{

  border-left: 0;
}

}
@media screen and (max-width:600px) {
  #column{
    display: none;
  }

}




</style>
