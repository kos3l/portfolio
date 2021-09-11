<template>
  <div id="mobile-projects" class="d-flex d-sm-none">
    <ul>
      <li v-for="work in works" :key="work.src" id="list-look-mobile">
        <a :href="work.src"> {{ work.name }} </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MobileProjects",
  data() {
    return {
      works: [
        {
          name: "@DOWN_UNDWER WEBSITE",
          src: "http://downunder.since.one/index.html",
        },

        {
          name: "@FANØ FLYER",
          src:
            "https://drive.google.com/file/d/1ci0IzsI_EWa0eNzthsxx4jcJjOlKrOmq/view?usp=sharing",
        },
        {
          name: "@VESTERHAVSGRUPPEN WEBSITE",
          src: "https://vesterhavsgruppen.netlify.app/",
        },
      ],
    };
  },
};
</script>

<style>
@media screen and (max-width: 600px) {
  #mobile-projects {
    width: 100vw;
    margin: 0;
    height: 40vh;
    border: 2px solid black;
    border-bottom: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding-top: 2vh;
    padding-right: 6vw;
    background-color: black;
  }
  .night #mobile-projects {
    border: 2px solid white;
    border-bottom: 0;
  }
  #list-look-mobile {
    list-style-type: none;
    font-size: 1rem;
    font-weight: 300;
    letter-spacing: 0.1rem;
    padding-bottom: 4vh;
    text-shadow: 3px 3px 3px #3cd5b7;
    padding: 0;
    padding-bottom: 4vw;
  }
  #list-look-mobile a {
    color: white;
  }
}
</style>
