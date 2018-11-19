<template>
  <div class="text-xs-center">
<h1>Egyszerű, ikonhoz kapcsolt badge, szöveges tartalommal</h1><br>
    <v-badge color="red" class="jel">
      <span slot="badge">!</span>
      <v-icon
        large
        color="dark-grey"
      >
        mail
      </v-icon>
    </v-badge><br/>
<img src="mail.png" alt="mail_badge" class="kep"><br/><br/>

<h1>Balra igazított, átfedő badge</h1><br/>
    <v-badge left color="blue" overlap>
      <span slot="badge">6</span>
      <v-icon
        large
        color="dark-grey"
      >
        shopping_cart
      </v-icon>
    </v-badge><br/>
<img src="shopping_cart.png" alt="mail_badge" class="kep"><br/><br/>

<h1>Szöveghez kapcsolt badge</h1><br/>
    <v-badge left color="blue">
      <span slot="badge">2</span>
      <span>Példa</span>
    </v-badge>
    <br/>
<img src="szoveg_badge.png" alt="mail_badge" class="kep"><br/><br/>

<h1>Ikont tartalmazó badge</h1><br/>
      <v-badge color="purple">
        <v-icon slot="badge" dark small>
          shopping_cart</v-icon>
        <span>
          Kosár
        </span>
      </v-badge>
      <br/>
<img src="ikon_badge.png" alt="mail_badge" class="kep"><br/><br/>
<h1>Láthatóság kapcsolása</h1>
<v-container fluid class="text-xs-center">
    <v-layout
      justify-space-between
      row
      wrap
    >
      <v-flex xs12>
        <v-btn
          color="indigo"
          class="white--text"
          @click="show = !show"
        >
          Kapcsolás
        </v-btn>
      </v-flex>

      <v-flex xs12 class="mt-5">
        <v-badge
          v-model="show"
          color="cyan"
          left
        >
          <span slot="badge">6</span>
          <v-icon
            large
            color="dark-grey"
          >shopping_cart</v-icon>
        </v-badge>

        <v-badge
          v-model="show"
          color="purple"
        >
          <span slot="badge">6</span>
          <v-icon large color="dark-grey">mail</v-icon>
        </v-badge>
      </v-flex>
    </v-layout>
  </v-container>
<img src="badge_kapcsol.png" alt="mail_badge" class="kep"><br/><br/>
<img src="badge_kapcsol_script.png" alt="mail_badge" class="kep"><br/><br/>

  </div>
</template>



<script>
import HelloWorld from "./components/HelloWorld";

export default {
  data() {
    return {
      show: true
    };
  }
};
</script>
<style>
.text-xs-center {
  margin: auto;
  padding: 20px;
}

.kep {
  width: 250px;
}

body {
  background-color: rgb(211, 211, 211);
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
}

.kep2 {
  width: 300px;
}

h1 {
  font-size: 16px;
}
</style>
