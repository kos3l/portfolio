<template>
    <div id="input-card">
        <form id="form-card">
            <label></label>
                <input type="text" id="input-box" v-model="message"  :multiline="true" placeholder="That's a nice input box right here...">
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
#form-card{

    width: 100%;
    height: 80%;
    display: flex;
    justify-content: center;
    align-items: center;
    
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

</style>