<template>
  <div id="project" :class="mode === 'day' ? 'day' : 'night'">
    <router-link :to="{ name: 'ProjectDetails', params: { id: project.id } }">
      <div id="project-inner">
        <div id="project-image-wrap">
          <img :src="project.src" class="image" />
        </div>
        <div id="project-text-wrap">
          <p class="text-center  text-uppercase ">
            {{ project.title }}
          </p>
        </div>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: "ProjectCard",
  props: ["project", "mode"],
};
</script>

<style>
* {
  margin: 0;
  padding-right: 0;
  box-sizing: border-box;
  text-decoration: none;
  color: black;
}

#project {
  display: flex;
  width: 37.5vw;
  margin-right: 0;
  margin-bottom: 0;
  justify-content: center;
  border-top: 2px solid black;
  background-color: white;
}
#project a {
  width: 100%;
}
#project-text-wrap {
  border-top: 2px solid black;
  margin: 0;
  padding-top: 4vh;
  font-weight: 300;
  letter-spacing: 0.1rem;
  font-size: 2rem;
}
#project-text-wrap p {
  color: black;
}
#project-inner {
  border-right: 2px solid black;
  width: 100%;
  height: 65vh;
  background-color: white;
}
#project-image-wrap {
  height: 50vh;
  background-color: white;
}

.image {
  width: 100%;
  height: 50vh;
  -webkit-filter: grayscale(100%); /* Safari 6.0 - 9.0 */
  filter: grayscale(100%);
  -webkit-transition: 0.3s ease-in-out;
  transition: 0.3s ease-in-out;
  object-fit: cover;
  object-position: 50% 40%;
}

.image:hover {
  filter: grayscale(0%);
}

.night #project #project-inner {
  border-right: 2px solid white;
  background-color: black;
  border-top: 2px solid white;
}

.night #project {
  border-top: none;
}

.night #project #project-text-wrap p {
  color: white;
}

@media screen and (max-width: 1200px) {
  #project {
    width: 100vw;
    height: auto;
    border-right: 2px solid black;
  }

  #project-inner {
    width: 100%;
    height: auto;
    border: 0;
  }
  #project-image-wrap {
    height: 25vh;
  }

  .image {
    height: 25vh;
  }
  #project-text-wrap {
    padding: 1rem;
    font-size: 1rem;
    border-top: 0;
  }
}
@media screen and (max-width: 600px) {
  #project {
    width: 100vw;
    margin: 0;
    height: auto;
    border: 2px solid black;
    background-color: white;
  }

  #project-inner {
    width: 100%;
    height: auto;
    border: 0;
    background-color: white;
  }

  .image {
    height: 25vh;
    -webkit-filter: none;
    filter: none;
    object-position: 70% 40%;
    border-bottom: 2px solid black;
  }
  #main-body {
    border: 0;
  }
  #profile {
    border-left: 2px solid black;
    border-right: 2px solid black;
  }
  #project-text-wrap {
    padding: 1rem;
    font-size: 0.9rem;
    border-top: 2px solid white;
  }

  #project-image-wrap {
    height: 25vh;
  }
  .night #project {
    border-bottom: 2px solid white;
    border-right: 2px solid white;
    border-left: 2px solid white;
    background-color: black;
  }

  .night #project #project-inner {
    border-right: 2px solid white;
    background-color: black;
    border-top: 2px solid white;
    background-color: black;
  }
}
</style>
