<template>
   <div id="info-card">
                        <div id="detail-content">
                        <p id="titles">> Email:</p>
                        <p id="my-info">{{ email }}</p>
                        <p id="titles">> Phone number:</p>
                        <p id="my-info">{{ phone }}</p>
                        </div>
                    <button id="card-button">COPY</button>
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
    }

}
</script>

<style>
#info-card{
    width: 46%;
    height: 16vw;
    background-color: #97EAD2;
    border: 2px solid black;
    height: 100%;
    display: flex;
    justify-content: flex-end;
    flex-direction: column;

}
#detail-content{
    width: 100%;
    height: 16vw;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    flex-direction: column;
    padding: 8vh 2vw 2vh 2vw;
}
#titles {
    font-size: 1.6vw;
    letter-spacing: 0.1vw;
    text-transform: uppercase;
    color: white;
    font-weight: 400;
    margin-bottom: 0.1vh;
    text-shadow: 3px 3px 3px #45CB9D;
}

#my-info{
    font-size: 1.3vw;
    letter-spacing: 0.1vw;
    color: white;
    margin-bottom: 3vh;
    font-weight: 400;
    text-shadow: 3px 3px 3px #45CB9D;
}
</style>