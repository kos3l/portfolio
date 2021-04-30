<template>
  <div class="About">
    <div id="bg">
      <v-row id="main-row">
        
        <v-col lg="2">
        </v-col>

        <v-col lg="8" id="middle">
          <Banner />
          <ArticleImage v-for="photo in photos" :key="photo.title" :photo="photo"/>
          <ArticleText  v-for="text in texts" :key="text.id" :text="text"/>
          
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
import ArticleText from '/src/components/ArticleText'
export default {
   name: 'About',
  components: {
    Banner,
    ArticleImage,
    ArticleText

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
      ],
      texts: [
        { 
          head: "INTRODUCTION",
          body: 'My name is Karolina Kosinska and I’m 20 year old Multimedia design student, based in Esbjerg, Denmark. I chose this education on Business Academy Southwest, since I have a wide range of interests. My first passion was drawing which with time evolved to be graphic design. While growing up I became drawn towards animation, 2D and 3D and languages. Front end web development allows me to be creative and solve problems, which I enjoy ever since I have started my upper secondary education with advanced maths. Therefore, working in this field is my main goal as it’s a point where all my passions meet.',
          id: 1
        },
        { 
          head: 'WORK EXPERIENCE',
          body: 'I have been doing freelance work up to this point. My main commissions were illustrations or icon designs. During my AP degree education I was working on a project called “Tinderbox” for 7-kanten so I also have experience in communication with clients.',
          id: 2
        },
        { 
          head: 'MY ROOTS',
          body: "I was born and raised in a small town called Brzeg Dolny in Poland. It may seem like a boring place, but it offered me many opportunities to be creative. In primary school I was a part of my town’s stop motion animation course where we created our own movies from scratch. Growing up in a country of contrasts, rich history, many problems and blossoming culture made me who I am now. It inspired me greatly and influenced to be always wondering how could we solve existing problems surrounding us. I always stay realistic and have a back up plan in case something goes wrong. ",
          id: 3
        },
        { 
          head: 'MINDSET',
          body: "I my opinion, there is nothing a person can’t learn. Given enough practice, energy and passion one can become good at any given field. I proved this to myself many times and I want to carry on with this notion further in my life. I have also learned my lesson on how stressful competitive environment can be, but my solution was to always stay humble, look up to other people and be inspired by them. When working with people, my rule number one is to avoid conflicts. I’m willing to work hard in order to find the best compromise. I’m a rather cheerful and calm person and I love to make jokes with colleagues. I’m too anxious to procrastinate so I always have everything done before the deadlines.",
          id: 4
        }
      ]
        }
    }

}
</script>

<style>

#bg{
  width: 100%;
  height: 500vh;
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
