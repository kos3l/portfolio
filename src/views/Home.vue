<template>
  <div class="home">

            <ProjectCard v-for="project in projects" :key="project.title" :project="project" />
            <router-view></router-view>

  </div>
  
</template>

<script>
import ProjectCard from "/Users/karolinakosinska/Desktop/portfolio/src/components/ProjectCard"
export default {
  name: 'Home',
  components: {
    ProjectCard,
  }, 
  data() {
    return {
      projects: [
        { 
          title: 'Down under',
          src: require('/src/assets/ilustrejszynFinished.png'),
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
          title: 'Fanø flyer',
          src: require('/src/assets/fano.png'),
          id: 4
        }
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
</style>
