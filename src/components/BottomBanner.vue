<template>
    <v-row id="outer-banner">
        <v-col id="inner-banner">
            <p id="movind-words">
                Owing to my ambitious personality, I chose advanced maths class in highschool, 
                even though I was an artistic person at the heart. It cost me 3 years of <i> suffering </i> but atleast I found out how much I enjoy solving problems and learned to never give up.
            </p>
        </v-col>
    </v-row>
</template>

<script>
export default {
    name: 'BottomBanner',

}
</script>

<style>
#outer-banner{
    height: 4vh;
    width: 100vw;
    background-color: white;

}
#inner-banner{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100%;

}
#movind-words{
    font-weight: 400;
    letter-spacing: 0.1rem;
    font-size: 1.3vw;
    margin: 0;
}

</style>