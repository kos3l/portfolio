<template>
  <div class="About">
    <div id="bg-projects">
      <v-row id="main-row-projects">
        
        <v-col lg="2">
        </v-col>

        <v-col lg="8" id="middle-projects">
          <Banner />
          <div v-if="id==1">
            <FanoText v-for="fano in fanos" :fano="fano" :key="fano.nr"/>
          </div>

          <div v-if="id==2">
            <DesignText description="Here is a collection of my best works I have made throughout the years. Majority was done in Adobe Photoshop and some in Illustrator."/>
          </div>

          <div v-if="id==3">
            <TinderText v-for="tinderbox in tinderboxes" :tinderbox="tinderbox" :key="tinderbox.nr"/>
          </div>

          <div v-if="id==4">
            <DuText v-for="downunder in downunders" :downunder="downunder" :key="downunder.nr"/>
          </div>
        </v-col>

        <v-col lg="2">
        </v-col>
      </v-row>
    </div>
   
  </div>
</template>

<script>
import Banner from '/src/components/Banner'
import FanoText from '/src/components/FanoText'
import DuText from '/src/components/DuText'
import TinderText from '/src/components/TinderText'
import DesignText from '/src/components/DesignText'
export default {
  components: {
    Banner,
    FanoText,
    DuText,
    TinderText,
    DesignText
    },
    props: ['id'],
    data() {
        return {
      fanos: [
        {
          description: "As one of my mandatory assignments during the first semester I made a flyer about an island next to Esbjerg called Fanø. It’s a extraordinary trip destination, because of it’s unique charm, nature and architecture. ",
          nr:1,

        },
        {
          description: "My first move was to do research and write my text for the flyer. Next, I have decided to take a trip there on my own and gather pictures from the town of Nordby and one of the beaches. I really value being able to experience the place before creating an advertisement in order to recreate it’s feeling in my work.  ",
          nr:2,

        },
        {
          description: "Since my time was very limited I didn’t create any sketches beforehand, I figured out the design and the layout while creating the flyer. I have mostly used InDesign, Photoshop and Illustrator while creating the flyer.",
          nr:3,

        }
      ],
      downunders: [
        {
          description: "Here you can see my first semester exam project I did in a group of four people. It was done only with the use of html and css as at the time, our course haven’t introduced any front-end frameworks yet. It was also my first website which I have fully created from scratch with my team. The theme for the project was “the sea” and the purpose was to make an informational website. We chose a topic of deep sea creatures. ",
          nr:1
        },
        {
          description: "The topic - Deep sea creatures have the appeal that can draw people’s interest as they are scary and seem alienlike. Based on our research how horror games on YouTube and scary stories like “creepypasta” gained a lot of attention throughout the years on the internet, we came to conclusion it was the right choice. Another reason for it was, how easily we could tie it with environmental issues such as plastic pollution and to make this educational website’s purpose meaningful.  ",
          nr:2
        },
        {
          description: "Our work began by brainstorming ideas, creating mirro mind maps, personas and surveys. After gathering enough data and inspiration I have created initial wireframes and mock ups. Through our design we wanted to created a dark and mysterious atmosphere. The navigation and layout was simple to put the most focus on the content. Our survey results, told us that majority of people see science information through videos on YouTube, hence each topic has at least one.",
          nr:3
        }
      ],
      tinderboxes: [
        {
          description: "During my second semester’s project week, we were appointed by 7-kantent, the biggest group of amateur actors group, which make plays since 70s to create a way to advertise their upcoming play called “Fyrtøjet”. It is a tale written by Christian Andersen. My group was assigned to create a game concept, which would spark interest of potential viewers and introduce them to the story. ",
          nr:1
        },
        {
          description: "After researching 7-kanten, the tale and establishing target group we sought to find the right game genre and suiting mechanics. Our conclusion was to create a mix of a arcade game and a story novel. In order to progress in the story and to be able to choose story options you need to gain action points through a Tetris like mini game. This project had many limitations such as the budget hence we planned the game to cover only the beginning of the story up until a cliffhanger moment.",
          nr:2
        },
        {
          description: "I have designed the characters, the mini game and did the last background with the dog in the cave, beside being a big part of creating the initial concept. Characters I have designed were meant to stay true to the tale but also look similar to the costumes 7-kanten already prepared",
          nr:3
        }
      ],
        }
    }

}
</script>

<style>
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
  border-top: 0;

}
</style>