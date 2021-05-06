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
                    <button id="card-button" v-on:click="copyToClipboard('karo7965@easv365.dk  +45 50398333')">COPY</button>
    </div>
</template>

<script>
export default {
    name: 'InfoCard',
    data() {
        return{
            email: 'karo7965@easv365.dk',
            phone: '+45 50398333'

        }
    },
    methods: {
         copyToClipboard(text) {
            var input = document.body.appendChild(document.createElement("input"));
            input.value = text;
            input.focus();
            input.select();
            document.execCommand('copy');
            input.parentNode.removeChild(input);
            }

}}
</script>

<style>
#info-card{
    width: 100%;
    height: 27vh;
    background-color: #97EAD2;
    border: 2px solid black;
    height: 100%;
    display: flex;
    justify-content: flex-end;
    flex-direction: column;

}
#contact-wrap{
    display: flex;
    flex-direction: row;
    height: 27vh;

}
#detail-content{
    width: 100%;
    height: auto;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;

}
#titles {
    font-size: 2vw;
    letter-spacing: 0.1vw;
    text-transform: uppercase;
    color: white;
    font-weight: 400;
    margin-bottom: 0.1vh;
    text-shadow: 3px 3px 3px #45CB9D;
}

#my-info{
    font-size: 1.5vw;
    letter-spacing: 0.1vw;
    color: white;
    margin-bottom: 3vh;
    font-weight: 400;
    text-shadow: 3px 3px 3px #45CB9D;
}

.night #info-card{
    border: 2px solid white;
    background-color: #97ead341;
}

#card-button:hover{
    background-color: black;
    color: white;

}

.night #card-button:hover{
    background-color: white;
    color: black;

}

@media screen and (max-width:1264px) {
    #info-card{
    width: 100%;
    height: 30vh;
    border: none;
    border-top: 2px solid black;
    

    }
    #detail-content{
        height: 30vh;
        align-items: center;
        padding: 2vh 2vw 0vh 2vw;
        

    }
    #titles {
        font-size: 2.5vw;
        
    }

    #my-info{
        font-size: 2vw;

    }
}
@media screen and (max-width:900px) {

    #middle-c{
    border-left: none;
    }
    #titles {
        font-size: 3.5vw;
        
    }

    #my-info{
        font-size: 3vw;

    }
    
}
@media screen and (max-width:600px) {

    #titles {
        font-size: 4vh;
        
    }

    #my-info{
        font-size: 3vh;

    }
    #info-card{
        height: 43vh;
    }
    #contact-wrap{
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding-bottom: 10vh;
    height: 27vh;
}
        #card-button:focus{
            background-color: black;
            color: white;

        }

        .night #card-button:focus{
            background-color: white;
            color: black;

        }

}
</style>