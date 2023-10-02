<template>
  <v-footer dark padless>
    <v-card flat tile class="black white--text py-12 px-5" width="100%">
      <v-row>
        <v-col cols="12" xs="12" sm="6" md="4" class="pa-16">
          <v-toolbar color="transparent" flat>
            <v-badge color="#D5F0DB" dot>
              <v-img src="1.png" contain width="30"></v-img>
            </v-badge>

            <v-toolbar-title class="ml-4">
              <span class="green--text">T</span><strong>okoku</strong>
            </v-toolbar-title>
          </v-toolbar>
          <v-card-text class="pt-0">
            <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-1 white--text"
              icon
              fab
              outlined
              small
            >
              <v-icon size="20px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>
        </v-col>
        <v-col cols="12" xs="12" sm="6" md="2">
          <v-card-text class="white--text pt-0">
            <h3>Tentang Kami</h3>
          </v-card-text>
          <v-card-text class="grey--text"> Cara Kerja</v-card-text>
          <v-card-text class="grey--text mt-n4"> Program </v-card-text>
          <v-card-text class="grey--text mt-n4"> Promosi </v-card-text>
          <v-card-text class="grey--text mt-n4"> Harga Bersahabat </v-card-text>
        </v-col>
        <v-col cols="12" xs="12" sm="6" md="2">
          <v-card-text class="white--text pt-0">
            <h3>Pengiriman</h3>
          </v-card-text>
          <v-card-text class="grey--text"> Bayar di tempat </v-card-text>
          <v-card-text class="grey--text mt-n4"> Metode Pembayaran </v-card-text>
          <v-card-text class="grey--text mt-n4"> Pengiriman Pesanan </v-card-text>
          <v-card-text class="grey--text mt-n4"> Pengembalian </v-card-text>
        </v-col>
        <v-col cols="12" xs="12" sm="6" md="4">
          <v-card-text class="white--text pt-0">
            <h3>Kontak</h3>
          </v-card-text>
          <v-card-text class="grey--text"> Tokokuadm </v-card-text>
          <v-card-text class="grey--text mt-n4">
            Bogor, Ciomas
          </v-card-text>
          <v-card-text class="grey--text mt-n4"> adm.tokoku.com </v-card-text>
          <v-card-text class="grey--text mt-n4"> -62857 8888 9999 </v-card-text>
        </v-col>
      </v-row>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: [
      "fab fa-apple",
      "fab fa-google-plus-g",
      "fab fa-twitter",
      "fab fa-facebook-f",
    ],
  }),
};
</script>

<style>
</style>