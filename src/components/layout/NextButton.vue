<template>
                <div id="next">
                    <router-link :to="{ name: 'ProjectDetails', params: { id: 2 }}"> project 1</router-link>
                </div>
</template>

<script>
export default {
    name: 'NextButton',
    props: ['id'],

}
</script>

<style>
#next{
    position: absolute;
    margin-bottom: 20vh;
    margin-left: 5vw;
    bottom: 0;
    color: white;
    font-weight: 300;
    letter-spacing: 0.1rem;
    font-size: 2vw;
}
</style>