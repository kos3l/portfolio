<template>

    <v-row id="footer-container" class="d-none d-sm-flex">
        <v-col id="inner-footer">
            <a href="https://github.com/kos3l" target="_blank" id="some"> @ GITHUB </a>
            <a href="https://www.linkedin.com/feed/" target="_blank" id="some"> @ LINKEDIN </a>
            <a href="https://www.instagram.com/pimpoqe/" target="_blank" id="some"> @ INSTAGRAM </a>
        </v-col>
        <v-col id="second-inner-footer">
            <p id="some-fun">I have a cat named Kropka, she's cute</p>
        </v-col>
    </v-row>
</template>

<script>
export default {

    name: 'Footer',
    


}
</script>

<style>

#footer-container{
    width: 100vw;
    height: 12vh;
    background-color: black;
    flex-direction: row;
    
    

}
#inner-footer{
    display: flex;
    justify-content: left;
    align-items: center;
    flex-direction: row;

}
#inner-footer a {
    margin-left: 30px;
}
#some{
    text-decoration: none;
    color: white;
    font-size:24px;
    font-weight: 900;
}
#second-inner-footer{
    background-color: black;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    margin-right: 30px;
    height: 100%;

}
#some-fun{
    color: white;
    font-size:24px;
    font-weight: 900;
    margin-bottom: 0;
}




</style>