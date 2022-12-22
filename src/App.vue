<template>
  <div id="app">
    <div class="card">
      <router-view />
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #ECEEF2;
  font-family: "Nunito", sans-serif;
}

.card {
  background: white;
  max-width: 620px;
  max-height: 100%;
  margin: 0 auto;
  margin-top: 50px;
  padding: 0 3vw;
  border-radius: 20px;
}

@media (max-width: 768px) {
  body {
    background: white;
    height: 100%;
  }
}
</style>
