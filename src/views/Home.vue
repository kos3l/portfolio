<template>
  <div class="home" :mode="mode">
            <Banner one="P" two="R"  three="O" four="J" five="E" six="C" seven="T" eight="S"/> 
            <ProjectCard v-for="project in projects" :key="project.title" :project="project"  :mode="mode"/>
            <MobileProjects />
            <router-view></router-view>

  </div>
  
</template>

<script>
import ProjectCard from "/Users/karolinakosinska/Desktop/portfolio/src/components/layout/ProjectCard"
import Banner from '/src/components/layout/Banner'
import MobileProjects from '/src/components/layout/MobileProjects'
export default {
  name: 'Home',
  components: {
    ProjectCard,
    Banner,
    MobileProjects
  }, 
  props: ['mode'],
  data() {
    return {
      projects: [
        { 
          title: 'Fanø flyer',
          src: require('/src/assets/Screenshot.png'),
          id: 1
        },
        { 
          title: 'Designs',
          src: require('/src/assets/foggyfeelings.jpg'),
          id: 2
        },
        { 
          title: 'Tinderbox',
          src: require('/src/assets/tinder.png'),
          id: 3
        },
        { 
          title: 'Down under',
          src: require('/src/assets/ilustrejszynFinished.png'),
          id: 4
        },
      ]
    }
  }
}
</script>


<style>
.home {
  display: flex;
  width: 100%;
  flex-wrap: wrap;
  flex-direction: row;
  background-color: white;


}
@media screen and (max-width:600px) {
  .home{
    padding-bottom: 10vh;
}
}

</style>
