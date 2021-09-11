<template>
  <div class="Contact">
    <div id="bg-c">
      <v-row id="main-row-c">
        <v-col lg="1" md="1" id="column"> </v-col>

        <v-col lg="10" md="10" sm="12" id="middle-c">
          <Banner one="H" two="E" three="L" four="L" five="O" />
          <div id="headline">
            <p>
              <i>Feel free to get in touch with me on my social media too!</i>
            </p>
          </div>
          <div id="some-mobile">
            <a href="https://github.com/kos3l" target="_blank" id="some-c">
              @ GITHUB
            </a>
            <a
              href="https://www.linkedin.com/feed/"
              target="_blank"
              id="some-c"
            >
              @ LINKEDIN
            </a>
            <a
              href="https://www.instagram.com/pimpoqe/"
              target="_blank"
              id="some-c"
            >
              @ INSTAGRAM
            </a>
          </div>

          <div id="text-wrapper">
            <div id="details">
              <p>CONTACT DETAILS:</p>
            </div>
          </div>
          <div id="wrapper1">
            <InfoCard />
          </div>
        </v-col>

        <v-col lg="1" md="1" id="column"> </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
import Banner from "/src/components/layout/Banner";
import InfoCard from "/src/components/InfoCard";
export default {
  name: "Contact",
  components: {
    Banner,
    InfoCard,
  },
};
</script>

<style>
#wrapper1 {
  width: 55vw;
  height: 60%;
  margin: 1vh 0vw 2vw 3.5vw;
  display: flex;
  justify-content: space-between;
}
#bg-c {
  width: 100%;
  height: auto;
  background-color: grey;
}
#main-row-c {
  height: auto;
  width: 100%;
  margin: 0;
}

#middle-c {
  background-color: white;
  padding: 0;
  border: 2px solid black;
  border-top: 0;
  border-bottom: 0;
}
#some-c,
#some-mobile {
  display: none;
}
#headline {
  letter-spacing: 0.1vw;
  font-size: 1.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5vw;
  height: 17vh;
  border-top: 2px solid black;
}
#text-wrapper {
  margin: 0;
  width: 100%;
  height: 5vh;
  display: flex;
  align-items: flex-end;
  font-weight: 900;
  letter-spacing: 0.1vw;
  justify-content: space-around;
  font-size: 1.5vw;
  padding-right: 1.4vw;
}

#card-button {
  width: 100%;
  min-height: 8vh;
  background-color: white;
  border-top: 2px solid black;
  font-weight: 300;
  font-size: 2vw;
}

.night #middle-c {
  background-color: black;
  border: 2px solid white;
}
.night #headline {
  border-top: 2px solid white;
  color: white;
}
.night #headline i {
  color: white;
}
.night #card-button {
  background-color: black;
  border-top: 2px solid white;
}
.night #card-button {
  color: white;
}
@media screen and (max-width: 1264px) {
  #wrapper1 {
    flex-direction: column;
    margin: 0;
    width: 100%;
    height: 47vh;
  }
  #text-wrapper {
    display: none;
  }
  #bg-c {
    width: 100%;
    height: 80vh;
    background-color: grey;
  }
  #main-row-c {
    height: 80vh;
    width: 100%;
    margin: 0;
  }
}
@media screen and (max-width: 958px) {
  #middle-c {
    border-left: none;
  }
  #headline {
    font-size: 1rem;
  }
  #card-button {
    font-size: 3vw;
  }
}
@media screen and (max-width: 600px) {
  #middle-c {
    border-left: 2px solid black;
    height: auto;
  }
  #wraper1 {
    height: 80vh;
  }
  #headline {
    padding: 2vh 2vw 0vh 2vw;
    font-size: 0.8rem;
    text-align: center;
  }
  #card-button {
    font-size: 6vw;
  }
  #main-row-c {
    height: 80vh;
  }
  #bg-c {
    height: auto;
  }
  #some-c {
    text-decoration: none;
    color: black;
    font-size: 0.8rem;
    font-weight: 900;
    display: block;
  }

  #some-mobile {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    width: 100%;
    height: 10vh;
  }
}
</style>
