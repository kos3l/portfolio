<template>
    <div class="Contact">
    <div id="bg-c">
        <v-row id="main-row-c">
            
            <v-col lg="2">
            </v-col>

            <v-col lg="8" id="middle-c">
                <Banner />


                <div id="text-wrapper">
                    <div id="write">
                        <p>WRITE ME HERE:</p>

                    </div>
                    <div id="details">
                        <p> MY DETAILS:</p>
                        <p></p>
                    </div>
                </div>
                <div id="wrapper1">
                    <div id="input-card">
                        

                    </div>
                    <div id="info-card">
                        
                    </div>

                </div>

            </v-col>

            <v-col lg="2">
            </v-col>
        </v-row>
    </div>
   
    </div>
</template>

<script>
import Banner from '/src/components/Banner'
export default {
     name: 'Contact',
  components: {
      Banner

  }

}
</script>

<style>

#wrapper1{
    width: 43vw;
    height: 37vh;
    margin: 0vw 3vw 3vw 3vw;
    display: flex;
    justify-content: space-between;

}
#bg-c{
  width: 100%;
  height: 75vh;
  background-color: grey;
}
#main-row-c {
  height: 100%;
  width: 100%;
  margin: 0;
}

#middle-c{
  background-color: white;
  padding: 0;
  border: 2px solid black;
  border-top: 0;

}
#input-card{
    width: 46%;
    background-color: grey;
    border: 2px solid black;
    height: 100%;

}
#info-card{
    width: 46%;
    background-color: grey;
    border: 2px solid black;
    height: 100%;

}
#text-wrapper{
    margin: 0;
    width: 100%;
    height: 100px;
    display: flex;

    align-items: flex-end;
    font-weight: 900;
}

#write{
    margin-left: 3vw;

}

#details{
    margin-left: 15vw;

}

</style>