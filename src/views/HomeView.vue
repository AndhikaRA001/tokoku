<template>
  <v-app>
    <Navbar />
    <v-container fluid>
      <v-row>
        <v-col cols="12">
          <v-card class="mx-auto rounded-xl" flat>
            <v-img src="cover5.jpg" max-height="90%" max-width="100%" contain>
              <v-card-title class="top ml-10">
                <h1 class="title1 white--text">PESAN KEBUTUHAN</h1>
              </v-card-title>
              <v-card-title class="ml-10 mt-n6">
                <h1 class="title2 white--text">HARIANMU DI TOKOKU</h1>
              </v-card-title>
              <v-card-text class="ml-10">
                <h2 class="green--text">#Gratis Ongkir</h2>
              </v-card-text>
              <v-card-text class="ml-10">
                <v-row>
                  <v-col cols="4">
                    <v-text-field label="Cari kebutuhan harianmu"
                    class="d-none d-sm-none d-md-flex"
                    filled solo prepend-inner-icon="mdi-magnify" flat rounded outline success
                    ></v-text-field>
                  </v-col>
                  <v-col cols="2" class="marginLeft">
                    <v-btn color="green" rounded dark x-large class="py-7 d-none d-sm-none d-md-flex">Cari</v-btn>
                  </v-col>
                </v-row>
              </v-card-text>
            </v-img>
          </v-card>
          <v-toolbar flat color="transparent">
            <v-toolbar-title class="text-h6">Kategori</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn-toggle v-model="toggle_exclusive" group color="#49D9A0">
              <v-btn>
                <v-icon>mdi-chevron-left</v-icon>
              </v-btn>
              <v-btn>
                <v-icon>mdi-chevron-right</v-icon>
              </v-btn>
            </v-btn-toggle>
          </v-toolbar>
          <Category />
          <v-toolbar flat color="transparent" class="mt-5">
            <v-toolbar-title class="text-h6">Produk Populer</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn rounded color="green" dark class="px-8">Liat Semua</v-btn>
          </v-toolbar>
          <Product />
          <v-card flat color="#E2F2E5" class="rounded-xl mt-8">
            <v-toolbar flat color="transparent" class="mb-4">
              <v-toolbar-title class="text-h6 mt-5">Popular Bundle Pack</v-toolbar-title>
            </v-toolbar>
            <Pack />
          </v-card>
          <v-card flat color="#FAFAFA" class="mt-8 py-5 px-16">
            <div 
            style="position: absolute; margin-left: auto; margin-right: auto; left: 0; right: 0; text-align: center;">
              <h3>Penilaian Konsumen</h3>
            </div>
            <Client />
          </v-card>
          <v-toolbar flat color="transparent" class="mt-8">
            <v-toolbar-title class="text-h6">
             <v-toolbar class="text-h6">Kerja Sama Bersama</v-toolbar>
            </v-toolbar-title>
          </v-toolbar>
          <Partner />
          <v-card flat color="#E2F2E5" class="rounded-xl mtop mbottom mx-10 pa-4" height="350">
            <v-row>
              <v-col cols="12" xs="12" sm="12" md="5">
                <v-card class="rounded-xl mt-n16 ml-16 mobile" outlined flat height="450" width="200">
                  <v-img src="mobile.png"></v-img>
                </v-card>
              </v-col>
              <v-col cols="12" xs="12" sm="6" md="7">
                <h1 class="mt-16">Download App</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. 
                   Eius reprehenderit suscipit dolorem, cumque nulla dolor 
                   doloremque deleniti incidunt alias repellat labore vitae 
                   molestiae maiores rem expedita placeat esse quia atque. 
                   Dolorum tempora ab, asperiores at quas minima iure reiciendis 
                   harum. Officia doloremque nam pariatur distinctio tempore 
                   ipsum modi quasi laborum.
                </p>
                <v-btn color="black" dark class="mb-10">
                  <v-icon color="white" left>fab fa-apple</v-icon>
                  App Store
                </v-btn>
                <v-btn color="black" dark class="ml-4 mb-10">
                  <v-icon color="white" left>fab fa-google-play</v-icon>
                  Play Store
                </v-btn>
              </v-col>
            </v-row>
          </v-card>
        </v-col> 
      </v-row>
    </v-container>
    <Footer />
  </v-app>
</template>

<script>
  import Navbar from '../components/Navbar'
  import Category from '../components/Category.vue'
  import Product from '../components/Product.vue'
  import Pack from '../components/Pack.vue'
  import Client from '../components/Client.vue'
  import Partner from '../components/Partner.vue'
  import Footer from '../components/Footer.vue'

  export default {
    data: () => ({
      toggle_exclusive:1,
    }),
    components: {
      Navbar,
      Category,
      Product,
      Pack,
      Client,
      Partner,
      Footer
    },
  }
</script>

<style>
.marginLeft{
  margin-left: -90px;
}
.mtop{
  margin-top: 100px;
}
.mbottom{
  margin-bottom: 100px;
}
.v-card.borderme{
  border: 2px solid green !important;
}
.v-card.borderout{
  border: 1px solid #d5f0db !important;
}
.v-btn:not(v-btn--round).v-size--default.add {
  min-width: 0px !important;
}
.theme--light.v-sheet--outlined.mobile{
  border: 2px solid black !important;
}
@media only screen and (max-width: 600px){
  h1.title1{
    font-size: 17px;
  }
  h1.title2{
    font-size: 17px;
  }
  .top{
    margin-top: 60px;
  }
}
@media only screen and (min-width: 600px){
  .top{
    margin-top: 70px;
  }
}
@media only screen and (min-width: 768px){
  .top{
    margin-top: 120px;
  }
}
</style>