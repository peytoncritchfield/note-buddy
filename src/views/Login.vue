<template>
    <div class="card">
      <div class="card-container mx-auto mt-5">
        <h3>Account Login</h3>
        <v-text-field
          class="input mx-auto mt-3"
          label="Your Email"
          outlined
          dense
          color="#1191F0"
          
        ></v-text-field>
        <v-text-field
          :append-icon="show ? 'mdi-eye' : 'mdi-eye-outline'"
          :type="show ? 'text' : 'password'"
          name="input-10-2"
          label="Password"
          class="input mx-auto mb-2"
          @click:append="show = !show"
          outlined
          hide-details="auto"
          dense
        ></v-text-field>
        <div class="link"> Forgot Password? </div>
        <v-btn
          color="#1C95F2"
          dark
          depressed
          width="100%"
          class="mt-5"
        > Continue </v-btn>
      </div>
    </div>
</template>

<script>
    export default {
        name: "App",
        data () {
            return {
                show: false,
                password: 'Password',
                rules: {
                emailMatch: () => (`The email and password you entered don't match`),
                },
            }
            }
    }
</script>

<style scoped>

.card {
  min-width: 200px;
  background-color: #fff;
  /* border-top-left-radius: 30px; */
  border-top-right-radius: 30px;
  position: fixed;
  top: 30vh;
  left: 0px;
  height: 80vh;
  width: 100vw;
  overflow: scroll;
}

.card-container {
  width: 80vw;
  min-width: 250px;
  max-width: 350px;
  margin-bottom: 100px;
}

.input {
  width: 100%;
}

.link {
  color: #1C95F2;
}

.continue-button {
  color: #fff;
  background-color: #1C95F2;
  height: 40px;
  width: 100%;
  border-radius: 05px;
  text-align: center;
}

</style>