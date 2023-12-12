<template>
  <div class="container text-center mb-3">
    <img src="@/assets/amigo-invisible.png" alt="Girl in a jacket" style="width:75%; max-width:1000px">
  </div>
  <RulesViewer />
  <CheckMate />
</template>

<script>
import RulesViewer from './components/RulesViewer.vue'
import CheckMate from './components/CheckMate.vue'

export default {
  name: 'App',
  components: {
    RulesViewer,
    CheckMate
  },
  methods: {
    btnCheckMate() {
      let user = document.getElementById("cboUser").value
      let password = document.getElementById("txtPassword").value

      switch (user) {
        case "Gerard":
          if (password == "6777") {
            alert("Te toca Jeremy");
          }
          break;
        case "Jeremy":
          if (password == "2786") {
            alert("Te toca Senen");
          }
          break;
        case "Jonas":
          if (password == "8689") {
            alert("Te toca Liriana");
          }
          break;
        case "Liriana":
          if (password == "0990") {
            alert("Te toca Jonas");
          }
          break;
        case "Rosi":
          if (password == "1786") {
            alert("Te toca Gerard");
          }
          break;
        case "Senen":
          if (password == "3436") {
            alert("Te toca Rosi");
          }
          break;
        default:
          alert("La contraseña no es correcta");
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
