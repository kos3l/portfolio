<template>
    <div id="input-card">
        <form id="form-card">
            <label> SEND ME A MESSAGE HERE... </label>
                <input type="text" id="input-box" v-model="message"  :multiline="true">
        </form>




    <button id="card-button">SEND</button>
    </div>
    
</template>

<script>
export default {
    name: 'ContactCard',
    data() {
        return {
            message: ''
        }
    }

}
</script>

<style>
#input-card{
    width: 60%;
    background-color: #97EAD2;
    border: 2px solid black;
    height: 100%;
    display: flex;
    align-items: flex-end;
    flex-direction: column;
    margin-right: 3.5vw;

}
#form-card{
    margin-left: 2vw;
    width: 100%;
    height: 80%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    
}
#form-card label{
    margin-top: 2vh;
    color: white;
    font-size: 1.3vw;
    letter-spacing: 0.1vw;
    font-weight: 400;
    text-shadow: 3px 3px 3px #45CB9D;
    
}
.night #input-card{
    border: 2px solid white;
    background-color: #97ead341;
}

#input-box{
    display: block;
    resize: none;
    width: 100%;
    height: 100%;
    color: white;
    padding: 0vh 2vw 13vh 2vw;
    font-size: 1.3vw;
    letter-spacing: 0.1vw;
    font-weight: 400;
    text-shadow: 3px 3px 3px #45CB9D;
    
}
@media screen and (max-width:1264px) {
    #input-card{
    height: 30vh;
    width: 100%;
    border: none;
    border-top: 2px solid black;
    

}
#form-card{
    margin-left: 2vw;
    width: 100%;
    height: 30vh;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    
}
#form-card label{
    margin-top: 1vh;
    color: white;
    font-size: 2vw;
    letter-spacing: 0.1vw;
    font-weight: 400;
    text-shadow: 3px 3px 3px #45CB9D;
    
}

}
@media screen and (max-width:900px) {

    #form-card label{
        
    font-size: 3vw;
    }
    
}
@media screen and (max-width:600px) {

    #form-card label{
    margin-top: 2vh;
    font-size: 5vw;
    }
}
</style>