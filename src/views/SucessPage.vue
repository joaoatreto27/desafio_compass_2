<template>
  <div class="SucessPage">
    <div id="header-sucess">
      <div class="logo">
        <img id="image-main" src="../assets/image.png" alt="Logo Intern Sing Up" />
      </div>
      <h1>Success</h1>
    </div>
    <div class="button-goback">
      <input
        @click="goBack"
        type="button"
        value="Go Back!"
        class="goback"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "SucessPage",
  methods: {
    goBack() {
      this.$router.push("/");
      this.$store.state.name = "";
      this.$store.state.email = "";
      this.$store.state.phone = "";
      this.$store.state.password = "";
      this.$store.state.checkbox = "";
      this.$store.state.birthday = "";
      localStorage.clear();
    },
  },
};
</script>

<style scooped>
.SucessPage {
  padding-top: 7vw;
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
  max-height: 650px;
}

#image-main {
    display: flex;
    width: 220px;
    height: 130px;
    margin: auto;
}

#header-sucess h1 {
  font-family: "Inter", sans-serif;
  margin-top: 10px;
  line-height: 1.5em;
  font-size: 2.25em;
  text-align: center;
  padding: 10px;
}

.button-goback {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items: center;
  margin: 10px auto 100px;
}

.goback {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 55px;
  font-size: 2.25em;
  width: 100%;
  height: 100%;
  border-radius: 10px;
  border: none;
  background: #0dbdbd;
  color: white;
  gap: 6px;
  cursor: pointer;
}

@media (max-width: 768px) {

  .SucessPage{
    height: 100%;
    width: 100%;
    padding-top: 0;
  }

  .button-goback {
    width: 90%;
    height: 20%;
    margin: 0 auto;
  }

  .goback {
    padding: 20px;
  }
}
</style>
