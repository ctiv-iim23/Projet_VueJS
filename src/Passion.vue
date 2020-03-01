<template>
  <v-container fluid>
    
    <div class="text-center">
          <h1><br><br>Mes expériences<br><br></h1>
      </div>
  <v-timeline>
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      :color="year.color"
      small
    >
      <template v-slot:opposite>
        <span
          :class="`headline font-weight-bold ${year.color}--text`"
          v-text="year.year"
        ></span><br><br>
        <span
          :class="py-3"
          v-text="year.text"
        ></span><br><br><br><br>
      </template>
    </v-timeline-item>
  </v-timeline>


      <div class="text-center">
          <h1><br>Mes compétences<br></h1>
      </div>
    <v-layout row>
      <v-flex
        pa-1
      >
        <v-card
          dark
          color="green darken-3"
        >
          <v-card-text>Langue : <br>
          Passions : <br>
          Logiciels maîtrisé : <br>
          Langage : <br></v-card-text>
        </v-card>
      </v-flex>
      <v-flex
        pa-1
      >
        <v-card
          dark
          color="green darken-1"
        >
          <v-card-text>Anglais B1, Espagnol A2<br>
          Jeux Vidéos, Voyager<br>
          Word, Excel, Poweerpoint, Photoshop, Indesign, Premiere, After Effect<br>
          C, HTML, CSS, Javascript, Vue<br></v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      years: [
        {
          color: 'green',
          year: 'Décembre 2010 : Pharmacie de Lognes',
          text: 'Stage de découverte en entreprise'
        },
        {
          color: 'blue',
          year: 'Juillet 2019 : Comunethic (Source Originelle)',
          text: 'Stage obligatoire : refonte du site Source Originelle, un site de Crowdfunding'
        },
        {
          color: 'brown',
          year: 'Septembre - Décembre 2019 : Artpaya',
          text: 'Freelence : refonte du site Artpaya, un site de e-commerce sur les objets de grandes valeurs'
        },
        {
          color: 'red',
          year: 'depuis Février 2020 : Autocyber',
          text: 'Freelance : aide avec le client à réaliser le projet "Cette année là" sur le Crowdfunding'
        }
      ]
    })
  }
</script>