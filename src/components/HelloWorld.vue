<template>
  <v-container class="fill-height">
    <v-sheet width="700" class="mx-auto  background">
      <v-row class="">
        <v-col class="margin-right">
      <v-form @submit.prevent class="">  
        <v-text-field
          v-model="number1" 
          label="Number 1" type="number"
        ></v-text-field>
        <v-text-field v-model="number2" label="Number 2" type="number"></v-text-field>
        <v-btn block class="mt-2" @click="topla">Topla</v-btn>
        <v-btn block class="mt-2" @click="cikartma">Çıkartma</v-btn>
        <v-btn block class="mt-2" @click="carpma">Çarpma</v-btn>
        <v-btn block class="mt-2" @click="bolme">Bölme</v-btn>
        <h1>Sonuç</h1>
        <p>{{ sonuc }}</p>
      </v-form>
      </v-col>
      <v-col class="bg-primary">
        <p>{{ sonuc > 100 ? "100 Değerinden Büyük" : "100 Değerinden Düşük" }}</p>
      </v-col>
    </v-row>
    </v-sheet>
  </v-container>
</template>

<script>
  export default{
    data(){
      return{
        number1: null,
        number2: null,
        sonuc : null,
      }
    },
    methods:{
      topla(){
      const toplam = +this.number1 + +this.number2;
      return this.sonuc = toplam;
    },
    cikartma(){
      const cikar = this.number1 - this.number2;
      return this.sonuc = cikar;
    },
    bolme(){
      const bolme = this.number1 / this.number2;
      return this.sonuc = bolme;
    },
    carpma(){
      const carpma = this.number1 * this.number2;
      return this.sonuc = carpma;
    },
    }
  }
</script>

<style>

.margin-right{
  margin-right: 100px;
  background-color: darkgoldenrod;
  color: white;
  box-shadow: inset(10);
}
.background{
  background-color: lightgreen;
 }
</style>