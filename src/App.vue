<template>
  <v-app>
  <v-card class="overflow-hidden">
    <v-app-bar
      absolute
      color="white"
      elevate-on-scroll
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>Christian TIV</v-toolbar-title>

      <v-spacer></v-spacer>


      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>
    </v-app-bar>
    
      <v-container>

  <v-parallax
    dark
    src="https://static.moniteurautomobile.be/imgcontrol/images_tmp/clients/moniteur/c680-d465/content/medias/images/news/33000/200/20/f1_2021_2.jpg"
    height="800"
  >
    <v-row
      align="center"
      justify="center"
    >
      <v-col class="text-center" cols="12">
        <h1 class="display-1 font-weight-thin mb-4">Bonjour à tous les amis ! Pour ceux qui me conaissent pas, vos grandes mères les Tiv qui montent sur une locomoTiv !!!</h1>
        <h4 class="subheading">Bienvenue dans mon portfolio</h4>
      </v-col>
    </v-row>
  </v-parallax>

    <v-content>
<v-card dark>
    <v-toolbar>
      <v-switch
        v-model="$vuetify.theme.dark"
        hide-details
        inset
        label="Theme Dark"
      ></v-switch>
    </v-toolbar>
</v-card>
      <HelloWorld/>
      <Parcours></Parcours>
      <MonParcours></MonParcours>
      <CV></CV>
      <Passion></Passion>
    </v-content>
    <v-carousel>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
      reverse-transition="fade-transition"
      transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
    <v-content>
      <Date></Date>
      <MyComponent></MyComponent>
    </v-content>
      </v-container>
  </v-card>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import MyComponent from './components/MyComponent';
import Parcours from './Parcours';
import MonParcours from './components/MonParcours';
import Passion from './Passion';
import Date from './components/Date';
import CV from './CV';

export default {
  
  name: 'App',

  components: {
    HelloWorld,
    MyComponent,
    MonParcours,
    Parcours,
    Passion,
    Date,
    CV
  },

  data () {
      return {
        items: [
          {
            src: "https://www.iim.fr/ecole-web/wp-content/themes/iim/img/logo-iim.png",
          },
          {
            src: 'https://newsroom.ionis-group.com/wp-content/uploads/2018/12/epitech-logo-quadri-baseline-anglais.png',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },
};
</script>
