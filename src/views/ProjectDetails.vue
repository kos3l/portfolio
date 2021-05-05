<template>
  <div class="About">
    <div id="bg-projects">
      <v-row id="main-row-projects">
        
        <v-col lg="1" md="1" sm="0" id="column">
        </v-col>

        <v-col lg="10" md="10" sm="12" id="middle-projects">
          <div v-if="id==1">
          <Banner one="F" two="L"  three="Y" four="E" five="R"/>
            <Fano v-for="fano in fanos" :key="fano.nr" :fano="fano"/>
          <div id="changeparam">
            <button id="totop" v-on:click="toTop"  > TO THE TOP</button> 
            <button id="next" > 
              <router-link :to="{ params: { id: 2 }} "><p>NEXT PROJECT</p></router-link>
            </button>
          </div>
          </div>

          <div v-if="id==2">
            <Banner one="A" two="R"  three="T"/>
            <v-col id="first-card">
              <p> This is a collection of my works I have done throughout the years. Most of them were done in Photoshop and some in Illustrator. Two of them were a study I did based on a picture. My favourite subject to draw are people, however I know the basics of perspective and environment design.
              </p>
            </v-col>
            <Design v-for="design in designs" :key="design.nr" :design="design"/>
            <div id="changeparam">
            <button id="totop" v-on:click="toTop"  > TO THE TOP</button> 
            <button id="next" > 
              <router-link :to="{ params: { id: 3 }} "><p>NEXT PROJECT</p></router-link>
            </button>
          </div>
          </div>

          <div v-if="id==3">
            <Banner one="G" two="A"  three="M" four="E"/>
            <Tinderbox v-for="tinderbox in tinderboxes" :key="tinderbox.nr" :tinderbox="tinderbox"/>
            <div id="changeparam">
            <button id="totop" v-on:click="toTop"  > TO THE TOP</button> 
            <button id="next" > 
              <router-link :to="{ params: { id: 4 }} "><p>NEXT PROJECT</p></router-link>
            </button>
          </div>
          </div>

          <div v-if="id==4">
            <Banner one="W" two="E"  three="B"/>
            <DownUnder v-for="downunder in downunders" :key="downunder.nr" :downunder="downunder"/>
            <div id="changeparam">
            <button id="totop" v-on:click="toTop"  > TO THE TOP</button> 
            <button id="next" > 
              <router-link :to="{ params: { id: 1 }} "><p>NEXT PROJECT</p></router-link>
            </button>
          </div> 
          </div>

        </v-col>

        <v-col lg="1" md="1" sm="0" id="column">
        </v-col>
      </v-row>
    </div>
   
  </div>
</template>

<script>
import Banner from '/src/components/layout/Banner'
import Fano from '/src/components/projects/Fano'
import DownUnder from '/src/components/projects/DownUnder'
import Tinderbox from '/src/components/projects/Tinderbox'
import Design from '/src/components/projects/Design'

export default {
  components: {
    Banner,
    Fano,
    DownUnder,
    Tinderbox,
    Design
    },
    props: ['id'],
    methods: {
      toTop() {
      this.$vuetify.goTo(0)
    }},
    data() {
        return {
          
      fanos: [
        {
          title: "INTRODUCTION",
          description: "As one of my mandatory assignments during the first semester I made a flyer about an island next to Esbjerg called Fanø. It’s a extraordinary trip destination, because of it’s unique charm, nature and architecture. ",
          nr:1,
          src: require('/src/assets/fano1.png')

        },
        {
          title: "PROCESS",
          description: "My first move was to do research and write my text for the flyer. Next, I have decided to take a trip there on my own and gather pictures from the town of Nordby and one of the beaches. I really value being able to experience the place before creating an advertisement in order to recreate it’s feeling in my work.  ",
          nr:2,
          src: require('/src/assets/fano2.png')

        },
        { title: "TOOLS",
          description: "Since my time was very limited I didn’t create any sketches beforehand, I figured out the design and the layout while creating the flyer. I have mostly used InDesign, Photoshop and Illustrator while creating the flyer.",
          nr:3,
          src: require('/src/assets/flowers.png')

        }
      ],
      downunders: [
        {
          title: "INTRODUCTION",
          description: "Here you can see my first semester exam project I did in a group of four people. It was done only with the use of html and css as at the time, our course haven’t introduced any front-end frameworks yet. It was also my first website which I have fully created from scratch with my team. The theme for the project was “the sea” and the purpose was to make an informational website. We chose a topic of deep sea creatures. ",
          nr:1,
          src: require('/src/assets/landingpageexample.png')
          
        },
        {
          title: "THE REASONING",
          description: "The topic - Deep sea creatures have the appeal that can draw people’s interest as they are scary and seem alienlike. Based on our research how horror games on YouTube and scary stories like “creepypasta” gained a lot of attention throughout the years on the internet, we came to conclusion it was the right choice. Another reason for it was, how easily we could tie it with environmental issues such as plastic pollution and to make this educational website’s purpose meaningful.  ",
          nr:2,
          src: require('/src/assets/fishexample.png')
        },
        {
          title: "PROCESS",
          description: "Our work began by brainstorming ideas, creating mirro mind maps, personas and surveys. After gathering enough data and inspiration I have created initial wireframes and mock ups. Through our design we wanted to created a dark and mysterious atmosphere. The navigation and layout was simple to put the most focus on the content. Our survey results, told us that majority of people see science information through videos on YouTube, hence each topic has at least one.",
          nr:3,
          src: require('/src/assets/bodyexample.png')
        }
      ],
      tinderboxes: [
        {
          title: "INTRODUCTION",
          description: "During my second semester’s project week, we were appointed by 7-kantent, the biggest group of amateur actors group, which make plays since 70s to create a way to advertise their upcoming play called “Fyrtøjet”. It is a tale written by Christian Andersen. My group was assigned to create a game concept, which would spark interest of potential viewers and introduce them to the story. ",
          nr:1,
          src: require('/src/assets/tinder.png')
        },
        { 
          title: "PROCESS",
          description: "After researching 7-kanten, the tale and establishing target group we sought to find the right game genre and suiting mechanics. Our conclusion was to create a mix of a arcade game and a story novel. In order to progress in the story and to be able to choose story options you need to gain action points through a Tetris like mini game. This project had many limitations such as the budget hence we planned the game to cover only the beginning of the story up until a cliffhanger moment.",
          nr:2,
          src: require('/src/assets/pies.png')
        },
        {
          title: "THE DESIGN",
          description: "I have designed the characters, the mini game and did the last background with the dog in the cave, beside being a big part of creating the initial concept. Characters I have designed were meant to stay true to the tale but also look similar to the costumes 7-kanten already prepared",
          nr:3,
          src: require('/src/assets/characters.jpg')
        }
      ],
        designs: [
          {
            nr:1,
            src: require('/src/assets/stelladiver.jpg')
          },
          {
            nr:2,
            src: require('/src/assets/foggyfeelings.jpg')
          },
          {
            nr:3,
            src: require('/src/assets/www.jpg')
          },
          {
            nr:4,
            src: require('/src/assets/ilustracja.png')
          },
          {
            nr:5,
            src: require('/src/assets/present copy.png')
          },
          {
            nr:6,
            src: require('/src/assets/present_vector.png')
          },
          {
            nr:7,
            src: require('/src/assets/something.jpg')
          },
          {
            nr:8,
            src: require('/src/assets/cwiczonko.png')
          },
          {
            nr:9,
            src: require('/src/assets/study1.png')
          },
          {
            nr:10,
            src: require('/src/assets/portfolioBG.jpg')
          },
          {
            nr:11,
            src: require('/src/assets/IMG_4123.jpg')
          }
        
        ]
        
    }},
    

}
</script>

<style>

#changeparam{
    border-top: 2px solid black;
    height: 10vh;
    width: 100%;
    display: flex;
    justify-content: space-between;
}
#next{

    color: black;
    font-weight: 300;
    letter-spacing: 0.1rem;
    font-size: 2vw;
    border-left: 2px solid black;
    width: 50%;
    

}
#next p{
    margin: 0;
}
#totop{
  width: 50%;
  color: black;
  font-weight: 300;
  letter-spacing: 0.1rem;
  font-size: 2vw;


}
#first-card{
  width: 100%;
  height: 50vh;
  border-top: 2px solid black;
  font-weight: 300;
  letter-spacing: 0.1rem;
  font-size: 1.5vw;
  padding: 3vw;
  display: flex;
}

#first-card p{
  display: flex;
  justify-content: center;
  align-items: center;
}

#bg-projects{
  width: 100%;
  height: auto;
  background-color: grey;
}
#main-row-projects {
  height: auto;
  width: 100%;
  margin: 0;
}

#middle-projects{
  background-color: white;
  padding: 0;
  border: 2px solid black;
  border-bottom: 0;
  border-top: 0;

}
@media screen and (max-width:1263px) {
    #first-card{

    height: 35vh;

  }
}
@media screen and (max-width:960px) {
  #column{
    display: none;
  }
  #middle-projects{
  border-left: 0;
}
  #first-card{
    font-size: 2.5vw;


  }

}
@media screen and (max-width:600px) {
  #column{
    display: none;
  }
  #first-card{
    border-left:2px solid black;
    font-size: 4vw;
    padding: 10vw;
  }

}
</style>