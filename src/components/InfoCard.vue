<template>
  <div id="info-card">
    <div id="contact-wrap">
      <div id="detail-content">
        <p id="titles">> Email:</p>
        <p id="my-info">{{ email }}</p>
      </div>
      <div id="detail-content">
        <p id="titles">> Phone number:</p>
        <p id="my-info">{{ phone }}</p>
      </div>
    </div>
    <button
      id="card-button"
      v-on:click="copyToClipboard('karo7965@easv365.dk  +45 50398333')"
    >
      COPY
    </button>
  </div>
</template>

<script>
export default {
  name: "InfoCard",
  data() {
    return {
      email: "karo7965@easv365.dk",
      phone: "+45 50398333",
    };
  },
  methods: {
    copyToClipboard(text) {
      var input = document.body.appendChild(document.createElement("input"));
      input.value = text;
      input.focus();
      input.select();
      document.execCommand("copy");
      input.parentNode.removeChild(input);
    },
  },
};
</script>

<style>
#info-card {
  width: 100%;
  height: 70vh;
  background-color: #97ead2;
  border: 2px solid black;
  height: 100%;
  display: flex;
  justify-content: flex-end;
  flex-direction: column;
}
#contact-wrap {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 70vh;
}
#detail-content {
  width: 100%;
  height: auto;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding: 3rem;
}
#titles {
  font-size: 2.2rem;
  letter-spacing: 0.1vw;
  text-transform: uppercase;
  color: white;
  font-weight: 400;
  margin-bottom: 0.1vh;
  text-shadow: 3px 3px 3px #45cb9d;
}

#my-info {
  font-size: 2rem;
  letter-spacing: 0.1vw;
  color: white;
  margin-bottom: 3vh;
  font-weight: 400;
  text-shadow: 3px 3px 3px #45cb9d;
}

.night #info-card {
  border: 2px solid white;
  background-color: #97ead341;
}

#card-button:hover {
  background-color: black;
  color: white;
}

.night #card-button:hover {
  background-color: white;
  color: black;
}

@media screen and (max-width: 1264px) {
  #info-card {
    width: 100%;
    height: 100%;
    border: none;
    border-top: 2px solid black;
  }
  #detail-content {
    height: 10vh;
    align-items: center;
    padding: 1rem;
  }
  #titles {
    font-size: 1.3em;
  }

  #my-info {
    font-size: 1.2rem;
  }
}
@media screen and (max-width: 900px) {
  #middle-c {
    border-left: none;
  }
  #titles {
    font-size: 3.5vw;
  }

  #my-info {
    font-size: 3vw;
  }
  #detail-content {
    padding: 1rem;
  }
}
@media screen and (max-width: 600px) {
  #detail-content {
    margin-top: 2rem;
  }
  #titles {
    font-size: 4vh;
  }

  #my-info {
    font-size: 3vh;
  }
  #info-card {
    height: 43vh;
    justify-content: space-between;
  }
  #middle-c {
    height: auto;
  }
  #contact-wrap {
    display: flex;
    flex-direction: column;
    justify-content: center;

    height: auto;
  }
  #card-button:focus {
    background-color: black;
    color: white;
  }

  .night #card-button:focus {
    background-color: white;
    color: black;
  }
}
</style>
