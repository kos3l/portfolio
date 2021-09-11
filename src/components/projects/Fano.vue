<template>
  <div id="slides-container">
    <v-col id="article-f">
      <div id="wrapper">
        <h1 id="name">{{ fano.title }}</h1>
        <p>{{ fano.description }}</p>
      </div>
    </v-col>
    <v-col id="display">
      <v-col id="image-wrap">
        <img :src="fano.src" class="picture" />
      </v-col>
      <v-col id="title">
        <p>PREVIEW</p>
      </v-col>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "Fano",
  props: ["fano"],
};
</script>

<style>
#article-f {
  padding: 6vw;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  border-top: 2px solid black;
  height: 70vh;
  width: 100%;
  background-color: white;
}

#article-f p {
  font-weight: 300;
  letter-spacing: 0.1rem;
  font-size: 1rem;
}

.night #article-f {
  background-color: black;
  border-top: 2px solid white;
}
.night #title {
  background-color: black;
}
#name {
  font-weight: 900;
  color: #c4c4c4;
  font-size: 3vw;
  padding-bottom: 2vh;
}
@media screen and (max-width: 1264px) {
  #article-f {
    height: auto;
  }
}
@media screen and (max-width: 600px) {
  #article-f p {
    font-size: 0.8rem;
  }
  #article-f {
    padding: 10vw;
    border-left: 2px solid black;
  }
  #display {
    border-left: 2px solid black;
  }
  #title {
    font-size: 0.9rem;
  }
}
</style>
