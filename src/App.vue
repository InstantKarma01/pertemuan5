<script setup>
import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'

const slide = ref(1)
const autoplay = ref(true)
</script>

<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://www.reshot.com/preview-assets/icons/XMJCBFTE78/computer-XMJCBFTE78.svg">
          </q-avatar>
          TOKO PURA-PURA
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs align="left">
        <q-route-tab to="/page1" label="Beranda" />
        <q-route-tab to="/page2" label="Processors" />
        <q-route-tab to="/page3" label="Graphic Cards" />
      </q-tabs>
    </q-header>

    <div class="carousel-container q-pa-md">
      <q-carousel
        animated
        v-model="slide"
        navigation
        infinite
        :autoplay="autoplay"
        arrows
        transition-prev="slide-right"
        transition-next="slide-left"
        @mouseenter="autoplay = false"
        @mouseleave="autoplay = true"
        class="rounded-carousel"
      >
        <q-carousel-slide :name="1" img-src="https://i.ytimg.com/vi/IH4CYoaZkNU/maxresdefault.jpg" />
        <q-carousel-slide :name="2" img-src="https://selular.id/wp-content/uploads/2022/09/13th-gen-intel-core-1-feat.jpg.rendition.intel_.web_.1648.927-1068x601.jpg" />
        <q-carousel-slide :name="3" img-src="https://blogs.nvidia.com/wp-content/uploads/2020/02/geforce-now-1280x680.jpg" />
        <q-carousel-slide :name="4" img-src="https://i.ytimg.com/vi/59It08CU028/maxresdefault.jpg" />
      </q-carousel>
    </div>

    <div class="q-pa-md">
    <div class="q-gutter-md row items-start">
      
      <q-card class="my-card" flat bordered style="max-width: 200px">
      <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRRXF4gF19xMQDqcdcHw2hFJaBJ2wR6nIlu7zLU-scy3g&s">

      <q-card-section>
        <div class="text-h6">AMD Ryzen 9 7950X3D - AM5</div>
        <q-separator />
        <div class="text-subtitle2">Rp10.299.000</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ lorem }}
      </q-card-section>
      </q-card>

      <q-card class="my-card" flat bordered style="max-width: 200px">
      <img src="https://www.static-src.com/wcsstore/Indraprastha/images/catalog/full//catalog-image/103/MTA-140384964/intel_intel_processor_core_i9_14900kf_-_lga1700_full01_miud2yop.jpg">

      <q-card-section>
        <div class="text-h6">Intel Core i9 14900KF - LGA1700</div>
        <q-separator />
        <div class="text-subtitle2">Rp9.500.000</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ lorem }}
      </q-card-section>
      </q-card>

      <q-card class="my-card" flat bordered style="max-width: 200px">
      <img src="https://images.tokopedia.net/img/cache/900/VqbcmM/2022/11/26/d46ed54f-fcb3-45a2-9889-4e9ae6e6773d.jpg">

      <q-card-section>
        <div class="text-h6">MSI GeForce RTX 4090 24GB GDDR6X - Gaming X TRIO</div>
        <q-separator />
        <div class="text-subtitle2">Rp33.150.000</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ lorem }}
      </q-card-section>
      </q-card>

      <q-card class="my-card" flat bordered style="max-width: 200px">
      <img src="https://down-id.img.susercontent.com/file/id-11134207-7r98w-lm7g0twxjlam3b">

      <q-card-section>
        <div class="text-h6">Gigabyte AMD Radeon RX 7900 XT GAMING OC 20G 20GB</div>
        <q-separator />
        <div class="text-subtitle2">Rp16.935.000</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ lorem }}
      </q-card-section>
      </q-card>

      <q-card class="my-card" flat bordered style="max-width: 200px">
      <img src="https://www.static-src.com/wcsstore/Indraprastha/images/catalog/full//catalog-image/103/MTA-150159729/brd-44261_asrock-intel-arc-a770-phantom-gaming-16gb-oc_full01-15df7f45.jpg">

      <q-card-section>
        <div class="text-h6">ASROCK Intel Arc A770 Phantom Gaming 16GB OC</div>
        <q-separator />
        <div class="text-subtitle2">Rp6.020.000</div>
      </q-card-section>

      <q-card-section class="q-pt-none">
        {{ lorem }}
      </q-card-section>
      </q-card>

    </div>
  </div>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer elevated class="bg-grey-8 text-white">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="https://www.reshot.com/preview-assets/icons/XMJCBFTE78/computer-XMJCBFTE78.svg">
          </q-avatar>
          <div>About Us</div>
        </q-toolbar-title>
        
      </q-toolbar>
      <div>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quidem blanditiis incidunt tenetur aperiam, ex aliquam nobis nisi atque tempora. Commodi provident vero aspernatur ducimus non culpa neque iusto perspiciatis aperiam!</div>
    </q-footer>

  </q-layout>
</template>

<script>
export default {
  setup () {
    const leftDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },
      slide,
      autoplay
    }
  }
}
</script>

<style scoped>
.carousel-container {
  max-width: 1250px;
  margin: 20px auto;
  padding-top: 98px; /* Menambahkan padding setara dengan tinggi header */
  border-radius: 20px;
}

.rounded-carousel {
  border-radius: 15px; /* Membulatkan sudut carousel */
  overflow: hidden; /* Memastikan gambar tidak keluar dari batas yang membulat */
}

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
