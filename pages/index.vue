<template>
  <div class="container">
     <NavBar/>
    <Header/>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue"
import Header from "@/components/Header.vue"

export default {
  components: {
    NavBar, 
    Header
  }
}
</script>

<style>



.container {
  margin: 0 auto;
  min-height: 100vh;
padding:0;
}

.title {
font-family: 'Public Sans', sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
