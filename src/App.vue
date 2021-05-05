<template>

    <v-app>
      
          <v-container id="skeleton" fluid>

                <v-row id="top-nav" >
                    <v-col id="dark-mode-btn" lg="3" md="3" sm="4">
                        <div id="links-abt">
                          <router-link :to="{ name: 'Home'}" id="links-abt">
                          >KAROLINA KOSINSKA
                          </router-link>
                        </div>
                    </v-col>
                    <v-col id="nav" lg="9" md="9" sm="8" cols="12">
                                  <router-link :to="{ name: 'About'}" >
                                    <button id="nav-button">
                                    <v-img id="icon-left" :src="require('/src/assets/circle.svg')"></v-img>
                                    <span id="links"> ABOUT ME </span>
                                    </button>
                                  </router-link>
                                  <router-link :to="{ name: 'Contact'}" >
                                    <button id="nav-button">
                                    <span id="links"> CONTACT </span>
                                    <v-img id="icon-right" :src="require('/src/assets/circle.svg')"></v-img>
                                    </button>
                                  </router-link>
                    </v-col>
                </v-row>
          
                <v-row id="main-body" >
                    <SideNav />

                    <v-col id="content" lg="9" md="9" sm="8" cols="12">
                        
                        <transition name="view">
                          <router-view/>
                        </transition>
                        
                        
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
                                  <v-img id="icon-mobile" :src="require('/src/assets/circle.svg')"></v-img>
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

import SideNav from './components/layout/SideNav'
import Footer from './components/layout/Footer.vue'
import BottomBanner from './components/layout/BottomBanner.vue'


export default {
  
  name: 'App',
  components: {
    SideNav,
    Footer,
    BottomBanner
  
    
    
  },
  data() {
    return {
      
    };
  },
  


};
</script>

<style>

#app{
  text-decoration: none;
  color: black;
  
}

#icon-left{
  width: 1.5vw;
  margin-right: 1vw;
}
#icon-right{
  width: 1.5vw;
  margin-left: 1vw;
}
#nav-button{
  display: flex;
  align-items: center;
}

.view-enter-active, .view-leave-active {
  transition: opacity 0.5s ease-in-out, transform 0.5s ease;
  border-left: 2px solid black;
}
.view-enter-active {
  transition-delay: 0.5s;
}
.view-enter {
  opacity: 0;
  transform: translateX(50px)
}
.view-enter-to {
  opacity: 1;
  transform: translateX(0px)
}
.view-leave {
  opacity: 1;
  transform: translateX(0px)
}
.view-leave-to {
  opacity: 0;
  transform: translateX(50px)
}


#content{
  padding: 0;
  
}
#links{
  font-weight: 500;
  letter-spacing: 0.1rem;
  font-size: 1.5vw;
  color: black;
  z-index: 10;
}
#links-abt{
  font-weight: 500;
  letter-spacing: 0.1rem;
  font-size: 1.5vw;
  color: black;
  text-decoration: none;
}
#nav{
  padding: 0px 6.5vw 0px 6.5vw;
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

@media screen and (max-width:1000px) {
  #links{
  font-size: 2vw;
}
  #nav{
  padding: 0px 40px 0px 40px;
  justify-content: space-between;
  align-items: center;
  display: flex;
  
}

}
@media screen and (max-width:600px) {
  .view-enter-active, .view-leave-active {
  transition: opacity 0.5s ease-in-out, transform 0.5s ease;
  border: 0;
}
  #top-nav{
    display: none;
     
  }
    #links-mobile{
    font-size: 2.5vh;
    height: 100%;
  }
  #dark-mode-btn{
    display: none
  }

  #bottom-nav {
    margin-bottom: 0;
    z-index: 44444;
    position: fixed;
    bottom: 0;
    width: 100%;
    height: 10vh;
    background-color: white;
    border: 2px solid black;
    display: flex;
    justify-content: space-around;
    align-items: center;
  
    
 }
  #bottom-bar{
    z-index: 4444;
    display: flex;
    justify-content: space-around;
    align-items: center;
    
  }

  #main-body{
    margin-top: 0;
    
  }
  #skeleton{
    padding-top:0;
  }
  #top-nav{
      display: none;
    }
    #content{
     
    height: 30vh;

  }
  #icon-mobile{
      max-width: 30px;
      height: 30px;
    }


}

  @import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
   
    #body {
      font-family: 'Poppins', sans-serif;
      }
  

</style>
