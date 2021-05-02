<template>
  <v-col id="article">
            <div id="wrapper">
                <p>{{ description }}</p>
            </div>

        </v-col>
</template>

<script>
export default {
    name:'DesignText',
    props: ['description']

}
</script>

<style>
#article{
    padding: 6vw;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    border-top: 2px solid black;
    height: 50vh;
    width: 100%;
    background-color: white;
}

#article h1{
    font-weight: 900;
    color: #C4C4C4;
    padding-bottom: 2vh;
}
#article p{
    font-weight: 300;
    letter-spacing: 0.1rem;
    font-size: 1vw;

}
</style>