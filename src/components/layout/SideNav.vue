<template>
  <v-col id="side-nav" lg="3" md="3" sm="4" cols="12" :class="(mode === 'day') ? 'day' : 'night' ">
              <v-col id="profile" >

                    
                      <div id="parent" lg="12" md="12" sm="12">
                      <v-img
                        :src="require('/src/assets/portpic1.jpg')" /> </div>
                    <span id="mds-mobile" >
                      <router-link :to="{ name: 'Home'}" id="link-mobile" > 
                        >KAROLINA KOSINSKA
                        >MULTIMEDIA DESIGN STUDENT
                      </router-link>
                    </span>
                    

              </v-col>
              <v-col id="side-section" lg="12" md="12" sm="12" class="d-none d-sm-flex" :class="(mode === 'day') ? 'day' : 'night' ">
                
                <div id="mds">
                  >MULTIMEDIA DESIGN STUDENT
                </div>
              
              <div id="list" 
                  data-aos="slide-right" 
                  data-aos-delay="10"
                  data-aos-duration="2000"
                  data-aos-easing="ease-in-out-cubic"
                  >
                  
                <ul>
                  <li v-for="work in works" :key="work.src" id="list-look">
                    <a :href="work.src"> {{ work.name }} </a>
                  </li>
                </ul>
              </div>

              </v-col>
              
          </v-col>
</template>

<script>

export default {
  name: 'SideNav',
  props: ['mode'],

  components: {},
  data() {
    return {
      works: [
        {
          name: '@DOWN_UNDWER WEBSITE',
          src:'http://downunder.since.one/index.html'
        },
        {
          name: '@TINDERBOX XD PROTOTYPE',
          src:'https://xd.adobe.com/view/b417a7a7-0186-4ca2-b1cf-ec95bc96ac3f-e144/'
        },
        {
          name: '@FANØ FLYER',
          src: 'https://drive.google.com/file/d/1ci0IzsI_EWa0eNzthsxx4jcJjOlKrOmq/view?usp=sharing'
        },
      ],
      currentPage: this.$router.currentRoute.path, 
    }
  }
    

  

}
</script>

<style>
#list{
  width: 20vw;
  position: absolute;
  bottom: 18vh;
  left: 2vw;

}
#list ul{
  padding: 0;
}
#list-look{
  list-style-type: none;
  font-size: 1.8vw;
  font-weight: 300;
  letter-spacing: 0.1rem;
  padding-bottom: 3vh;
  text-shadow: 3px 3px 3px #D39BE8;
  
}
#list-look a{
  text-decoration: none;
  color: black;
}

#parent{
  width: 10vw;
  height: auto;
}
#mds-mobile{
  display: none;

}


#side-nav{
  border-right:2px solid black;
  padding: 0;
  background: linear-gradient(0deg, rgba(221,203,239,1) 10%, rgba(255,255,255,1) 100%);
  

}

.night #side-nav {
  border-right:2px solid white;
  padding: 0;
  background: linear-gradient(0deg, rgba(255,255,255,1) 10%, rgba(0,0,0,1) 70%);

}
.night #side-nav #profile{
  border-bottom: 2px solid white;
  padding: 0;
  background-color: black;

}
.night #side-section #mds {
  color: white;
  background:  rgba(237,170,222,0);
}
.night #side-section{
  background:  rgba(237,170,222,0);
}


#profile{
  background-color: white;
  border-bottom: 2px solid black;
  height: 312px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

#side-section{
  padding: 30px 20px 20px 30px;
  justify-content: space-between;
  align-items: center;
  flex-direction: column;


}

#mds {
  font-size: 3vw;
  font-weight: 300;
  margin-bottom: 20px;
  letter-spacing: 0.1rem;
}

@media screen and (min-width:1540px) {

    #profile{
    height: 490px;
    }
 }
 @media screen and (max-width:1100px) {
    #parent{
      width: 17vw;
    }
    #mds {
      font-size: 4.5vw;
      font-weight: 300;
    }
}

 @media screen and (max-width:600px) {
    #side-nav{
        border-right: 0;
        border-top: 2px solid black;
    }
    #profile{
        height: 30vh;
        display: flex;
        justify-content: right;
        padding-left: 45px;
        flex-direction: row;
        transform: translateY(2px);
    }
    #parent{
      width: 30vw;
    }
    #mds-mobile{
      font-size: 5vw;
      font-weight: 300;
      margin-left: 30px;
      display: block;
      text-decoration: none;
      color: black;
    }
    #link-mobile{
      text-decoration: none;
      color: black;
    }
    #list{
      display: none;
    }
}
</style>