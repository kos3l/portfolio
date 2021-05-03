<template>
  <v-col id="side-nav" lg="3" md="3" sm="4" cols="12" >
              <v-col id="profile" lg="12" md="12" sm="12">

                    
                      <div id="parent">
                      <v-img
                        :src="require('/src/assets/portpic1.jpg')" /> </div>
                    <span id="mds-mobile" >
                      <router-link :to="{ name: 'Home'}" id="link-mobile" > 
                        >KAROLINA KOSINSKA
                        >MULTIMEDIA DESIGN STUDENT
                      </router-link>
                    </span>
                    

              </v-col>
              <v-col id="side-section" lg="12" md="12" sm="12" class="d-none d-sm-flex" >
                
                <div id="mds">
                  >MULTIMEDIA DESIGN STUDENT
                </div>
              </v-col>
          </v-col>
</template>

<script>

export default {
  name: 'SideNav',
  

}
</script>

<style>

#side-nav{
background: linear-gradient(0deg, rgba(221,203,239,1) 0%, rgba(255,255,255,1) 70%);



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
  justify-content: center;
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
        border-bottom: 0;
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
}
</style>