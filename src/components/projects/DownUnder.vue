<template>
  <div id="slides-container">
    <v-col id="article-d">
      <div id="wrapper">
        <h1 id="name">{{ downunder.title }}</h1>
        <p>{{ downunder.description }}</p>
      </div>
    </v-col>
    <v-col id="display">
      <v-col id="image-wrap">
        <img :src="downunder.src" class="picture d-none d-sm-flex" />
        <img :src="downunder.mobile" class="picture d-flex d-sm-none" />
      </v-col>
      <v-col id="title">
        <p>PREVIEW</p>
      </v-col>
    </v-col>
  </div>
</template>

<script>
export default {
  name: "DownUnder",
  props: ["downunder"],
};
</script>

<style>
#article-d {
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

#article-d h1 {
  font-weight: 900;
  color: #c4c4c4;
  padding-bottom: 1.5rem;
}
#article-d p {
  font-weight: 300;
  letter-spacing: 0.1rem;
  font-size: 1.3rem;
}
#name {
  font-weight: 900;
  color: #c4c4c4;
  font-size: 3vw;
  padding-bottom: 2vh;
}
.night #article-d {
  background-color: black;
}
@media screen and (max-width: 1264px) {
  #article-d {
    height: auto;
  }
}
@media screen and (max-width: 600px) {
  #article-d {
    height: auto;
  }
  #article-d p {
    font-size: 0.8rem;
  }
  #article-d {
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
