<template>
  <v-row justify="center" class="space px-16 pb-5">
    <v-col cols="12" xs="12" sm="6" md="4" v-for="(pack, i) in packs" :key="i">
      <v-card class="mx-auto rounded-xl" max-width="300" color="" flat outlined>
        <div align="center" justify="center">
          <v-img
            max-height="300"
            max-width="300"
            contain
            :src="pack.img"
          ></v-img>
        </div>

        <v-card-title class="">{{ pack.title }}</v-card-title>
        <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{
          pack.subtitle
        }}</v-card-title>
        <v-card-title class="mt-n4">{{ pack.price }}</v-card-title>

        <v-card-actions class="mx-2 mt-n4">
          <v-btn outlined class="mt-n2 add">
            <v-icon color="#330066" @click="decrement"> mdi-minus </v-icon>
          </v-btn>

          <strong class="mx-2" v-text="bpm"></strong>
          <v-btn outlined class="mt-n2 add">
            <v-icon color="#330066" @click="increment"> mdi-plus </v-icon>
          </v-btn>
          <v-spacer></v-spacer>
          <v-btn class="mx-2 mt-n3" fab dark small color="#330066">
            <v-icon dark> mdi-shopping </v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
      bpm: 1,
    packs: [
      { img: "p1.png", title: "LENOVO", subtitle:"CPUi76thGen,Ram(8)GB, GPU2400,SSD512", price: "$850" },
      { img: "p2.png", title: "MSI", subtitle: "AMDRYZEN6,Ram(16)GB,RTX3050,1TB", price: "$730" },
      { img: "p3.png", title: "ASUS", subtitle: "CPUi510thGen,Ram(32)GB,GPU2600,1TB", price: "$904" },
      { img: "p4.png", title: "ASUS", subtitle: "CPUi79thGen,Ram(8)GB,GPU3200,SSD512", price: "$680" },
      { img: "p5.png", title: "ASUS", subtitle: "CPUi710thGen,Ram(16)GB,GPU2600,1TB", price: "$990" },
      { img: "p6.png", title: "MSI", subtitle: "AMDRYZEN5,Ram(32)GB,RTX3020,SSD512", price: "$890" },
    ],
  }),
   methods: {
      decrement () {
        this.bpm--
      },
      increment () {
        this.bpm++
      },
     
    },
};
</script>

<style>
</style>