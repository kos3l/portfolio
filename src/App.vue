<template>

    <v-app>
          <v-container id="skeleton" fluid>

                <v-row id="top-nav" >
                    <v-col id="dark-mode-btn" lg="3" md="3" sm="0" class="d-none d-sm-flex">
                      <button>
                        <v-icon left> mdi-checkbox-blank-circle-outline</v-icon>
                        <span id="links">DARK MODE</span>
                      </button>
                    </v-col>
                    <v-col id="nav" lg="9" md="9" sm="12" cols="12">
                                  <router-link :to="{ name: 'About'}" >
                                    <button>
                                    <v-icon left> mdi-checkbox-blank-circle-outline</v-icon>
                                    <span id="links"> ABOUT ME </span>
                                    </button>
                                  </router-link>
                                  <router-link :to="{ name: 'Contact'}" >
                                    <button>
                                    <span id="links"> CONTACT </span>
                                    <v-icon right>mdi-checkbox-blank-circle-outline</v-icon>
                                    </button>
                                  </router-link>
                    </v-col>
                </v-row>
          
                <v-row id="main-body" >
                    <SideNav />
                    <v-col id="content" lg="9" md="9" sm="8" cols="12">
                        <Banner /> 
                        <router-view></router-view>
                    </v-col>
                </v-row>




            <v-row id="bottom-nav" class=".d-flex .d-sm-none">
              <v-col id="bottom-bar" cols="12">
              </v-col>
            </v-row>
          </v-container>
      </v-app>
</template>

<script>

import SideNav from './components/SideNav'
import Banner from './components/Banner.vue'


export default {
  
  name: 'App',
  components: {
    SideNav,
    Banner
  
    
    
  },

  data: () => ({
    
   
  }),
};
</script>

<style>

#app{
  text-decoration: none;
  color: black;
  
}
#content{
  padding: 0;
}
#links{
  font-weight: 900;
  letter-spacing: 0.1rem;
  font-size: 25px;
  color: black;
}
#nav{
  padding: 0px 40px 0px 40px;
  justify-content: space-between;
  align-items: center;
  display: flex;
  font-size: 27px;
  
}
#top-nav{
  border: 2px solid black;
  height: 78px
  
  

}
#dark-mode-btn{
  border-right: 2px solid black;
  padding: 0px 40px 0px 40px;
  justify-content: space-between;
  align-items: center;
  display: flex;
  font-size: 27px;
}
#main-body{
  height: 100vh;
  border: 2px solid black;
  border-top: 0;
}
@media screen and (min-width:1440px) {

  #banner{
    height: 245px;
  }
}

@media screen and (max-width:600px) {
  #top-nav{
    display: none;
  }
 
  #bottom-bar{
    border: 2px solid black;
    border-top: 0;
    height: 10vh;
    position: fixed;
  }

  #main-body{
    margin-top: 0;
    height: 90vh;
  }
  #skeleton{
    padding-top:0;
  }
  #top-nav{
      display: none;
    }
    #content{

    height: 60vh;
    border-bottom: 2px solid black;
  }


}

  @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
   
    #body {
      font-family: 'Poppins', sans-serif;
      }
  

</style>
