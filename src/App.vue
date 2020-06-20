<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <br />

          <h1 style="color: white">WOD-DAR</h1>
            <h2 style="color: white">STRONA W BUDOWIE</h2>
        <button @click="whichColorComponent = 'appBlue'" class="btn btn-primary">O NAS</button>
        <button @click="whichColorComponent = 'appGreen'" class="btn btn-primary">TECHNOLOGIE</button>
        <button @click="whichColorComponent = 'appRed'" class="btn btn-primary">KONTAKT</button>
        <button @click="whichColorComponent = 'appWhite'" class="btn btn-primary">DANE TECHNICZNE POMP</button>
        <hr />
        <component :is="whichColorComponent"></component>
      
        <p style="color: white">kontakt: (+48) 603-651-601, NIP 9561540951</p>
      </div>
    </div>
  </div>
</template>

<script>
import Blue from "@/components/Blue.vue";
import Green from "@/components/Green.vue";
import Red from "@/components/Red.vue";
import White from "@/components/White.vue";

export default {
  data: function() {
    return {
      whichColorComponent: "appBlue"
    };
  },
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
  padding: 0;
  margin: 0;
  width: 100%;
}
body {
  background-color:rgb(79, 160, 187);
}
h1 {
  width: 100%;
  font-size: 6rem;
  text-align: center;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
h2 {
  width: 100%;
  font-size: 3rem;
  text-align: center;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
}
</style>
