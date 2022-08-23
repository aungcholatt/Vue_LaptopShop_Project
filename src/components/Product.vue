<template>
  <v-row justify="center" class="space px-16">
    <v-col
      cols="12"
      xs="12"
      sm="6"
      md="4"
      v-for="(product, i) in products"
      :key="i"
    >
      <v-card class="mx-auto rounded-xl" max-width="300" color="" flat outlined>
        <div align="center" justify="center">
          <v-img
            max-height="300"
            max-width="300"
            contain
            :src="product.img"
          ></v-img>
        </div>

        <v-card-title class="">{{ product.title }}</v-card-title>
        <v-card-title class="grey--text text-grey-darken-1 caption mt-n6">{{
          product.subtitle
        }}</v-card-title>
        <v-card-title class="mt-n4">{{ product.price }}</v-card-title>

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
    products: [
      { img: "pr1.png", title: "ASUS", subtitle: "CPUi510thGen,Ram(32)GB,GPU2600,1TB", price: "$790" },
      { img: "pr2.png", title: "MSI", subtitle: "AMDRYZEN5,Ram(32)GB,RTX3020,SSD512", price: "$980" },
      { img: "pr3.png", title: "ASUS", subtitle: "CPUi710thGen,Ram(16)GB,GPU2600,1TB", price: "$785" },
      { img: "pr4.png", title: "ASUS", subtitle: "CPUi76thGen,Ram(8)GB,GPU2400,SSD512", price:"$940" },
      { img: "pr5.png", title: "LENOVO", subtitle:"CPUi79thGen,Ram(8)GB,GPU3200,SSD512", price: "$965" },
      { img: "pr6.png", title: "ASUS", subtitle: "CPUi510thGen,Ram(32)GB,GPU2600,1TB", price: "$590" },
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