<template>
    <div class="Contact">
    <div id="bg-c">
        <v-row id="main-row-c">
            
            <v-col lg="2">
            </v-col>

            <v-col lg="8" id="middle-c">
                <Banner one="H" two="E" three="L" four="L" five="O"/>
                <div id="headline">
                    <p> <i>Feel free to contact me on my social media too!</i></p>
                </div>


                <div id="text-wrapper">
                    <div id="write">
                        <p>WRITE ME HERE:</p>

                    </div>
                    <div id="details">
                        <p> CONTACT DETAILS:</p>
                    </div>
                </div>
                <div id="wrapper1">
                    <ContactCard />
                    <InfoCard />
                        
                    

                </div>

            </v-col>

            <v-col lg="2">
            </v-col>
        </v-row>
    </div>
   
    </div>
</template>

<script>
import Banner from '/src/components/layout/Banner'
import ContactCard from '/src/components/ContactCard'
import InfoCard from '/src/components/InfoCard'
export default {
    name: 'Contact',
    components: {
            Banner,
            ContactCard,
            InfoCard

    }

}
</script>

<style>

#wrapper1{
    width: 43vw;
    height: 40%;
    margin: 0vw 3vw 3vw 3vw;
    display: flex;
    justify-content: space-between;


}
#bg-c{
  width: 100%;
  height: auto;
  background-color: grey;
}
#main-row-c {
  height: auto;
  width: 100%;
  margin: 0;
}

#middle-c{
  background-color: white;
  padding: 0;
  border: 2px solid black;
  border-top: 0;
  border-bottom: 0;
  
}
#input-card{
    width: 46%;
    background-color: #97EAD2;
    border: 2px solid black;
    height: 100%;
    display: flex;
    align-items: flex-end;
    flex-direction: column;

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
#text-wrapper{
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

#card-button{
    width: 100%;
    min-height: 8vh;
    background-color: white;
    border-top: 2px solid black;
    font-weight:300;
    font-size: 2vw;
    
}


</style>