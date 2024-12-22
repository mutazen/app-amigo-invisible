<template>
    <div class="container">
      <form>
        <div class="mb-3">
          <label for="user" class="form-label">¿Quién eres?</label>
          <select class="form-select" id="cboUser" aria-label="Default select example">
            <option selected>Pincha para selecionar tu nombre</option>
            <option value="Gerard">Gerard</option>
            <option value="Jeremy">Jeremy</option>
            <option value="Jonas">Jonas</option>
            <option value="Liriana">Liriana</option>
            <option value="Rosi">Rosi</option>
            <option value="Senen">Senen</option>
            <option value="Elena">Elena</option>
          </select>
        </div>
        <div class="mb-3">
          <label for="exampleInputPassword1" class="form-label">Password</label>
          <input type="password" class="form-control" id="txtPassword">
        </div>
        <button type="submit" class="btn btn-primary" v-on:click="checkMate">Ver quien me ha tocado</button>
      </form>
    </div>
  </template>

  <script>

  export default {
    name: 'CheckMate',
    props: {
      msg: String
    },
    methods: {
      checkMate: function () {

        let user = document.getElementById("cboUser").value
        let password = document.getElementById("txtPassword").value

        switch(user) {
          case "Gerard":
            if (password == "6777") {
              alert("Te toca Liriana")
            } else {
              alert("La contraseña no es correcta")
            }
          break;
          case "Jeremy":
            if (password == "2786") {
              alert("Te toca Jonas")
            } else {
              alert("La contraseña no es correcta")
            }
          break;
          case "Jonas":
            if (password == "8689") {
              alert("Te toca Elena")
            } else {
              alert("La contraseña no es correcta")
            }
          break;
          case "Liriana":
            if (password == "0990") {
              alert("Te toca Gerard")
            } else {
              alert("La contraseña no es correcta")
            }
          break;
          case "Rosi":
            if (password == "1786") {
              alert("Te toca Senen")
            } else {
              alert("La contraseña no es correcta")
            }
          break;
          case "Senen":
            if (password == "3436") {
              alert("Te toca Rosi")
            } else {
              alert("La contraseña no es correcta")
            }
          break;
          case "Elena":
            if (password == "3436") {
              alert("Te toca Jeremy")
            } else {
              alert("La contraseña no es correcta")
            }
          break;
          default:
            alert("No has dicho quien eres");
        }
      }
    }
  }

  </script>

  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  form {
    margin: 20px 0 0;
  }

  </style>
