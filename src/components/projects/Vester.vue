<template>
  <div id="slides-container">
    <v-col id="article-t">
      <div id="wrapper">
        <h1 id="name">{{ vester.title }}</h1>
        <p>{{ vester.description }}</p>
      </div>
    </v-col>
    <v-col id="display">
      <v-col id="image-wrap">
        <img :src="vester.src" class="picture d-none d-sm-flex" />
        <img :src="vester.mobile" class="picture d-flex d-sm-none" />
      </v-col>
      <v-col id="title">
        <p>PREVIEW</p>
      </v-col>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "Vester",
  props: ["vester"],
};
</script>

<style>
#article-t {
  padding: 6vw;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  border-top: 2px solid black;
  height: auto;
  width: 100%;
  background-color: white;
}

#article-t h1 {
  font-weight: 900;
  color: #c4c4c4;
  padding-bottom: 1.5rem;
}
#article-t p {
  font-weight: 300;
  letter-spacing: 0.1rem;
  font-size: 1.3rem;
}
#image-wrap {
  height: 60vh;
}
#name {
  font-weight: 900;
  color: #c4c4c4;
  font-size: 3vw;
  padding-bottom: 2vh;
}
.night #article-t {
  background-color: black;
  border-top: 2px solid white;
}
@media screen and (max-width: 1264px) {
  #article-t {
    height: auto;
  }
}
@media screen and (max-width: 600px) {
  #article-t p {
    font-size: 0.8rem;
  }
  #article-t {
    border-left: 2px solid black;
    padding: 10vw;
  }
  #display {
    border-left: 2px solid black;
  }
  #title {
    font-size: 0.9rem;
  }
  .picture {
    height: auto;
  }
  #image-wrap {
    height: auto;
  }
}
</style>
