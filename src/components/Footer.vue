<template>
    <v-row id="footer-container">
        <v-col id="inner-footer">
            <h1> {{ medialink.some }} </h1>
        </v-col>
    </v-row>
</template>

<script>
export default {

    name: 'Footer',
    props: ['medialink'],


}
</script>

<style>

#footer-container{
    width: 100%;
    height: 300px;
    background-color: pink;
}

</style>