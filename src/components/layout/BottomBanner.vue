<template>
    <v-row id="outer-banner">
        <v-col id="inner-banner">
            <div id="move1" class="move">
                PROXIMITY
            </div>
            <div id="move2" class="move">
                SIMILARITY
            </div>
            <div id="move3" class="move">
                CLOSURE
            </div>
            <div id="move4" class="move">
                CONTINUITY
            </div>
            <div id="move5" class="move">
                COMMON FATE
            </div>
            <div id="move6" class="move">
                CONTINUING LINE
            </div>
        </v-col>
    </v-row>
</template>

<script>
import anime from 'animejs';
    
export default {
    name: 'BottomBanner',
    
    mounted() {
            var tl = anime.timeline({
                easing: 'easeInOutSine',
                duration: 9000,
                loop:true,
                });

            tl
                .add({
                targets: '#move6',
                translateX:1920,
                })
                .add({
                targets: '#move5',
                translateX:1920,
                
                },'-=8000')
                .add({
                targets: '#move4',
                translateX:1920,

                },'-=8000')
                .add({
                targets: '#move3',
                translateX:1920,

                },'-=8000')
                .add({
                targets: '#move2',
                translateX:1920,

                },'-=8000')
                .add({
                targets: '#move1',
                translateX: 1920,

                },'-=8000');

                 var tl1 = anime.timeline({
                easing: 'easeInOutSine',
                duration: 9000,

                loop:true,
                });

            tl1
                .add({
                targets: '#move6',
                translateX:1920,
                })
                .add({
                targets: '#move5',
                translateX:1920,
                
                },'-=8000')
                .add({
                targets: '#move4',
                translateX:1920,

                },'-=8000')
                .add({
                targets: '#move3',
                translateX:1920,

                },'-=8000')
                .add({
                targets: '#move2',
                translateX:1920,

                },'-=8000')
                .add({
                targets: '#move1',
                translateX: 1920,

                },'-=8000');


  
}
}


    
    
    


</script>

<style>
#outer-banner{
    height: 4vh;
    width: 100vw;
    background-color: white;
    border-top: 2px solid black;

}
#inner-banner{
    height: auto;
    display: flex;
    align-items: center;
    padding: 0;

}
.move{
    font-weight: 400;
    letter-spacing: 0.1rem;
    font-size: 1.5vw;
    overflow: hidden;
}


</style>