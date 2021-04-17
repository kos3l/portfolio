<template>
  <nav>
    <v-toolbar flat app id="nav">
      <v-toolbar-title>
        
        <button class="text-uppercase">
          <span class="font-weight-bold">About</span>
        </button>

        <button class="text-uppercase">
          <span class="font-weight-bold"> Contact</span>
        </button>

      </v-toolbar-title>
      

    </v-toolbar>
  </nav>
</template>

<script>
export default {
    name: 'NavBar',
    data() {

    },
}
</script>

<style>
#nav {
  border: 2px solid black;
  
}
</style>