<template>

    <v-app>
          <v-container id="skeleton" fluid>

                <v-row id="top-nav" >
                    <v-col id="dark-mode-btn" lg="3" md="3" sm="0">
                        <div id="links-abt">
                          <router-link :to="{ name: 'Home'}" id="links-abt">
                          >KAROLINA KOSINSKA
                          </router-link>
                        </div>
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
                        
                        <router-view></router-view>
                    </v-col>
                </v-row>
                <BottomBanner />
                <Footer />




            <v-row id="bottom-nav" class=".d-flex .d-sm-none">
              <v-col id="bottom-bar" cols="12">
                <router-link :to="{ name: 'About'}" >
                                    <button>
                                    <span id="links-mobile"> ABOUT ME </span>
                                    </button>
                                  </router-link>
                                  <v-icon left> mdi-checkbox-blank-circle-outline</v-icon>
                                  <router-link :to="{ name: 'Contact'}" >
                                    <button>
                                    <span id="links-mobile"> CONTACT </span>
                                    </button>
                                  </router-link>
              </v-col>
            </v-row>
            
          </v-container>
      </v-app>
</template>

<script>

import SideNav from './components/SideNav'
import Footer from './components/Footer.vue'
import BottomBanner from './components/BottomBanner.vue'


export default {
  
  name: 'App',
  components: {
    SideNav,
    Footer,
    BottomBanner
  
    
    
  },


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
  font-weight: 800;
  letter-spacing: 0.1rem;
  font-size: 1.5vw;
  color: black;
}
#links-abt{
  font-weight: 400;
  letter-spacing: 0.1rem;
  font-size: 1.5vw;
  color: black;
  text-decoration: none;
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
  height: 78px;
  border-left: 0;
}
#dark-mode-btn{
  border-right: 2px solid black;
  justify-content: left;
  padding-left: 30px;
  align-items: center;
  display: flex;
  font-size: 27px;

}
#main-body{
  height: auto;

  border-top: 0;
}
#bottom-nav{
  display: none;
}
@media screen and (max-width:1100px) {
    #nav{
  padding: 0px 40px 0px 40px;
  justify-content: space-between;
  align-items: center;
  display: flex;
  font-size: 27px;
  
}
#dark-mode-btn{
  display: none
}
}

@media screen and (max-width:600px) {
  #top-nav{
    display: none;
     
  }
  #links-mobile{
  font-size: 25px;
}
#dark-mode-btn{
  display: none
}
 
 #bottom-nav {
    z-index: 44444;
    position: fixed;
    bottom: 0;
    width: 100%;
    height: 10vh;
    background-color: white;
    border: 2px solid black;
    display: block;
  
    
 }
  #bottom-bar{
    z-index: 4444;
    display: flex;
    justify-content: space-around;
    align-items: center;
  
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
