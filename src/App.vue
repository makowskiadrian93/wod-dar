<template>
<transition>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <br />

          <h1 style="color: white">WOD-DAR</h1>
          <h2 style="color: white">ODWADNIANIE IGŁOFILTRAMI</h2>
            <div class="buttons">
        <button @click="whichColorComponent = 'appBlue'" class="btn btn-primary">O NAS</button>
        <button @click="whichColorComponent = 'appGreen'" class="btn btn-primary">TECHNOLOGIE</button>
        <button @click="whichColorComponent = 'appRed'" class="btn btn-primary">KONTAKT</button>
        <button @click="whichColorComponent = 'appWhite'" class="btn btn-primary">DANE TECHNICZNE POMP</button>
        <button @click="gallery = !gallery" class="btn btn-primary">GALERIA</button>
        <transition name="fade">
          <p v-if="gallery">ZDJĘCIA</p>
          </transition>
        </div>
        <component :is="whichColorComponent"></component>
      <div class="container">
        </div>
          
       
        <p style="color: white">kontakt: (+48) 603-651-601, NIP 9561540951</p>
      </div>
    </div>
  </div>
  </transition>
</template>

<script>
import Blue from "@/components/Blue.vue";
import Green from "@/components/Green.vue";
import Red from "@/components/Red.vue";
import White from "@/components/White.vue";

export default {
  data: function() {
    return {
      whichColorComponent: "appBlue",
  
    };
  },
  
gallery: true,

  components: {
    appBlue: Blue,
    appGreen: Green,
    appRed: Red,
    appWhite: White
  }
};
</script>

<style>
body, html {
  offset: 20px;
  padding: 20px;
  margin: 20px;
  width: 90%;
}
body {
  background-color:rgb(79, 160, 187);
  offset: 20px;
  padding: 20px;
}
h1 {
  width: 100%;
  font-size: 6rem;
  text-align: center;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
h2 {
  width: 100%;
  font-size: 2rem;
  text-align: center;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
.container {
  display: grid;
  
}
.item {
  -moz-text-size-adjust: 100%;
}
.h2 {
  font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif }

button {
  background-color :#008CBA;
  border: none;
  color: white;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
}
.buttons {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-gap: 10px;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 1s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>


