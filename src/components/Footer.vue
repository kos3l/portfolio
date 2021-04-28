<template>

    <v-row id="footer-container">
        <v-col id="inner-footer">
            <a href="https://github.com/kos3l" target="_blank" id="some"> @ GITHUB </a>
            <a href="https://www.linkedin.com/feed/" target="_blank" id="some"> @ LINKEDIN </a>
            <a href="https://www.instagram.com/pimpoqe/" target="_blank" id="some"> @ INSTAGRAM </a>
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
    height: 10vh;
    background-color: black;
    

}
#inner-footer{
    display: flex;
    justify-content: space-around;
    align-items: center;
    flex-direction: row;

}
#some{
    text-decoration: none;
    color: white;
    font-size:27px;
    font-weight: 900;


}


</style>