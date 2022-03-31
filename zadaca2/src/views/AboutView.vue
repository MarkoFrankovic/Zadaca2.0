<template>
  <v-form>
    <v-container>
      <v-row>
        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Regular"
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Regular"
            placeholder="Placeholder"
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Solo"
            solo
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Solo"
            placeholder="Placeholder"
            solo
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Filled"
            filled
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Filled"
            placeholder="Placeholder"
            filled
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Outlined"
            outlined
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          sm="6"
          md="3"
        >
          <v-text-field
            label="Outlined"
            placeholder="Placeholder"
            outlined
          ></v-text-field>
        </v-col>
      </v-row>
    </v-container>
  </v-form>
</template>

<script>
/* eslint-disable */
let objekt = {
name: "AboutView",
data: function() {
  return{
    commits: [],
  };
},

async mounted(){
  let podatci = await fetch("https://agify.io/");
  let podatci2 = await fetch("https://genderize.io/");
  let podatci3 = await fetch("https://nationalize.io/");

  console.log(podatci);
  console.log(podatci2);
  console.log(podatci3);

  let rezultati = await podatci.json();
  let rezultati2 = await podatci2.json();
  let rezultati3 = await podatci3.json();

console.log(rezultati);
console.log(rezultati2);
console.log(rezultati3);

this.commits = rezultati;
this.commits = rezultati2;
this.commits = rezultati3;

}
}
</script>
