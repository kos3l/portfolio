<template>
  <div id="slides-container">
    <v-col id="article">
      <div id="wrapper">
        <h1 id="name">{{ article.head }}</h1>
        <p>{{ article.body }}</p>
      </div>
    </v-col>
    <v-col id="display">
      <v-col id="image-wrap">
        <img :src="article.src" class="picture d-none d-sm-flex" />
        <img :src="article.mobile" class="picture d-flex d-sm-none" />
      </v-col>
      <v-col id="title">
        <p>{{ article.title }}</p>
      </v-col>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "ArticleMe",
  props: ["article", "mode"],
};
</script>

<style>
#slides-container {
  width: 100%;
  height: auto;
}
#display {
  padding: 0;
}
#image-wrap {
  padding: 0;
  border-top: 2px solid black;
  height: 60vh;
  overflow: hidden;
}
#title {
  border-top: 2px solid black;
  font-weight: 300;
  letter-spacing: 0.1rem;
  font-size: 1.5vw;
  display: flex;
  align-items: center;
  justify-content: center;
}
#title p {
  margin: 0;
}
.picture {
  object-fit: cover;
  width: 100%;
  height: 100%;
  overflow: hidden;
}
#article {
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

.night #article {
  border-top: 2px solid white;
  background-color: black;
}
.night #article h1 {
  color: white;
}

.night #image-wrap {
  border-top: 2px solid white;
}
.night #title {
  border-top: 2px solid white;
}
#article h1 {
  font-weight: 900;
  color: #c4c4c4;
  padding-bottom: 3vh;
}
#article p {
  font-weight: 300;
  letter-spacing: 0.1rem;
  font-size: 1.3rem;
}

@media screen and (max-width: 1263px) {
  #article h1 {
    font-size: 1.3rem;
  }
  #article p {
    font-size: 1rem;
  }
  #article {
    height: 50vh;
  }
}
@media screen and (max-width: 600px) {
  #article {
    padding: 10vw;
    border-left: 2px solid black;
    height: auto;
  }
  #article h1 {
    font-size: 0.8rem;
  }
  #article p {
    font-size: 0.7rem;
  }
}
</style>
