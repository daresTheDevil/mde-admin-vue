<template>

  <v-container fluid class="ma-0 pa-0">
    <v-jumbotron 
      :gradient="gradient"
    dark
    height="500px"
    src="https://cdn.vuetifyjs.com/images/parallax/material2.jpg"
    >
    
    <v-layout row wrap>
      <v-flex xs4 offset-xs2 pt-5>
    <v-card
      class="ma-3 transparent"
      flat
      raised
    >
      <v-card-title primary-title>
          <div>
            <h3 class="display-3 mb-0 font-weight-bold">Yo, MDE!</h3>
            <div>Like KD in the commercial. <br>But this is our app.</div>
          </div>
        </v-card-title>
      <v-card-actions>
          <v-btn color="primary" to="/signup">Sign Up</v-btn>
        <v-btn to="/signin">Sign In</v-btn>
        </v-card-actions>
    </v-card>
      </v-flex>
    </v-layout>
    
    </v-jumbotron>
  </v-container>
</template>

<script>
export default {
  data() {
    return { gradient: 'to top right, rgba(63,81,181, .7), rgba(25,32,72, .7)', }
  }
};
</script>