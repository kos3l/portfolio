<template>
<v-app>
      <v-navigation-drawer app id="left-nav" :permanent="$vuetify.breakpoint.smAndUp">
        <v-toolbar-tile>
          <button  id="dark-mode-btn">
            <v-icon id="circle" left> mdi-checkbox-blank-circle-outline</v-icon>
            <span>DARK MODE</span>
          </button>
        </v-toolbar-tile>
      </v-navigation-drawer>

      <v-app-bar app flat id="right-nav">
        <v-toolbar-title id="about-btn" >
            <button>
              <router-link :to="{ name: 'About'}" >
              <v-icon id="circle" left> mdi-checkbox-blank-circle-outline</v-icon>
              <span id="nav-link"> ABOUT ME </span>
              </router-link>
            </button>
        </v-toolbar-title>

        <v-spacer></v-spacer>

        <button id="dark-mode">
            <v-icon>mdi-circle-half-full</v-icon>
        </button>

          <v-spacer></v-spacer>

        <v-toolbar-title>
            <button>
              <router-link :to="{ name: 'Contact'}" >
              <span id="nav-link"> CONTACT </span>
              <v-icon id="circle" right>mdi-checkbox-blank-circle-outline</v-icon>
              </router-link>
            </button>
          </v-toolbar-title>
      </v-app-bar>
</v-app>
</template>

<script>
export default {
    name: 'NavBar',
    data() {
      return {
        links: [
          {title:'About me', route: '/about'},
          {title:'Contact', route: '/contact'}
        ]
        
      }

    },
}
</script>

<style>
#right-nav{
  border: 2px solid black;
  padding: 0rem 3rem 0rem 3rem;
  border-left: 0;

}

#left-nav {
  border: 2px solid black;
  font-size: 20px;
  padding: 0rem 0rem 0rem 0rem;


  
}



#dark-mode {
  margin: 1rem;
  display: none;
}

#right-nav a{
  
  text-decoration: none;
  color: black;
  font-weight: 900;
  letter-spacing: 0.1rem;
  font-size: 20px;
  
}

#dark-mode-btn {

  border-bottom: 2px solid black;
  width: 100%;
  height: 61px;
  font-weight: 900;
  letter-spacing: 0.1rem;
  padding-top: 2.5px;

}

#dark-mode-btn a {
  font-weight: 900;
  letter-spacing: 0.1rem;
  
}

#circle {
  padding-bottom: 3px;
}


@media screen and (max-width:600px){
  #right-nav {
    border: 2px solid black;
    position: absolute;
    top:93vh;
    padding: 0 0.4rem 0 0.2rem;
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    
}
  #dark-mode{
    margin:1.5rem;
    display: block;

  }
  #nav-link {
    font-size: 17px;
  }
 
  
}

</style>