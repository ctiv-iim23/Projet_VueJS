<template>
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
</template>

<script>
  export default {
    data: () => ({
      years: [
        {
          color: 'cyan',
          year: 'Né le 12/01/1996 à Paris'
        },
        {
          color: 'pink',
          year: '2007 - 2011 : Collège du Segrais, Lognes',
          text: 'Diplôme Obtenu : Diplôme National du Brevet (mention Assez-Bien)'
        },
        {
          color: 'green',
          year: '2011 - 2015 : Lycée Emily Brontë, Lognes',
          text: 'Diplôme Obtenu : Bac S (spé math)'
        },
        {
          color: 'blue',
          year: '2015 - avril 2018 : EPITECH',
          text: 'Connaissance langage C. Quitté début avril 2018.'
        },
        {
          color: 'orange',
          year: 'depuis 2018 : IIM',
          text: 'Actuellement dans axe Développement Web'
        }
      ]
    })
  }
</script>