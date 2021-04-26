<template>
  <v-col id="side-nav" lg="3" md="3" sm="4" cols="12" >
              <v-col id="profile" lg="12" md="12" sm="12">

                    <router-link :to="{ name: 'Home'}" id="parent">
                      <v-img
                        :src="require('../assets/portpic1.jpg')"
                        
                      />
                    </router-link>

              </v-col>
              <v-col id="side-section" lg="12" md="12" sm="12" class="d-none d-sm-flex" >
                <span id="mds">
                  MULTIMEDIA DESIGN STUDENT
                </span>
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
background: linear-gradient(0deg, rgba(221,203,239,1) 0%, rgba(255,255,255,1) 60%);

}
#parent{
  width: 200px;
  height: auto;
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
}

#side-section{
  padding: 30px 10px 10px 30px
}

#mds {
  font-size: 3.5vw;
  font-weight: 300;
}

@media screen and (min-width:1540px) {

    #profile{
    height: 490px;
    }
 }

 @media screen and (max-width:600px) {
    #side-nav{
        border-right: 0;
        border-top: 2px solid black;
    }
    #profile{
        height: 30vh;
    }
}
</style>