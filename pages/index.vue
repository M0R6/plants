<template>
  <div class="josef">
    <!-- <div id="disini" class="w-screen h-[56px] border-0 p-1 m-0 bg-black" :class="{ 'hidden': hidden }">
      <div @click="hideIt" class="cursor-pointer">
        <div class="inline-block p-2">
          <font-awesome-icon class="h-6 ml-1 mt-1 cursor-pointer text-white" icon="xmark" />
        </div>
        <a href="https://sndo.ffm.to/55mdjb6" target="_blank">
          <div class="mt-[-56px] text-center p-[12px] text-2xl">
            <h1 class="text-white">
              <span>Stream</span>
              <span class="text-blue-300">MORG's "Wait On You"</span>
              <span>now!</span>
            </h1>
          </div>
        </a>
      </div>
    </div>
    <nav class="w-full bg-gradient-to-r from-gray-900 via-gray-800 to-gray-900 text-white py-5 px-4 shadow-lg">
      <div class="container mx-auto flex justify-center items-center">
      <ul class="flex flex-col md:flex-row space-y-4 md:space-y-0 md:space-x-12 text-center">
        <li>
        <a href="#spotify" class="relative font-medium text-lg hover:text-green-400 transition-colors duration-300 group">
          Spotify
          <span class="absolute left-0 bottom-0 w-0 h-0.5 bg-green-400 group-hover:w-full transition-all duration-300"></span>
        </a>
        </li>
        <li>
        <a href="#youtube" class="relative font-medium text-lg hover:text-red-400 transition-colors duration-300 group">
          YouTube
          <span class="absolute left-0 bottom-0 w-0.5 bg-red-400 group-hover:w-full transition-all duration-300"></span>
        </a>
        </li>
        <li>
        <a href="#contact" class="relative font-medium text-lg hover:text-purple-400 transition-colors duration-300 group">
          Contacts
          <span class="absolute left-0 bottom-0 w-0 h-0.5 bg-purple-400 group-hover:w-full transition-all duration-300"></span>
        </a>
        </li>
      </ul>
      </div>
    </nav> -->
    <div class="bg-container mx-auto w-screen h-screen border-0 p-0 m-0" :style="backgroundStyle">
      <div class="flex-auto text-center text-4xl">
        <div class="flex flex-col items-center justify-center h-full">
          <!-- <h1 class="pt-[15px] text-white josef2">
            <span>Morgan</span> <br />
            <span>Room</span> <br />
            <span>Records</span>
          </h1> -->
          <div class="flex justify-center items-center flex-col">
            <a href="https://instagram.com/nrfntr" target="_blank">
              <v-img class="mx-auto mt-3 d-flex justify-center" height="300" width="300" :src="require('~/assets/images/mrgn.svg')"></v-img>
            </a>
            <h1 class="m-7 text-center text-3xl text-white josef2">in colaboration with</h1>
            <a href="https://www.instagram.com/agrisouvenir.id/" target="_blank"> 
              <v-img class="mx-auto mt-3 d-flex justify-center" height="150" width="275" :src="require('~/assets/images/agri.svg')"></v-img>
            </a>
          </div>
        </div>
      </div>
      <div>
        <div class="flex justify-center items-center mt-10 p-4">
          <div class="max-w-md p-6 bg-white rounded-lg shadow-lg">
            <h2 class="text-2xl font-bold text-gray-800 text-center mb-4">Terima Kasih</h2>
            <p class="text-gray-600 text-center">
                Bapak-Ibu Guru pengampu pelajaran jurusan Rekayasa Perangkat Lunak: Pak Rusdi, Pak Haris, Bu Diah, Bu Titi Sari, Bu Reny, Bu Rosyi, Bu Dinda atas bimbingan dan dukungannya dalam proses pembelajaran di Skansaba selama 3 tahun ini. Semoga menjadi
                amal jariyah yang terus mengalir pahalanya, dan semoga Bapak-Ibu selalu diberikan kesehatan, kebahagiaan, serta keberkahan dalam setiap langkah kehidupan. Aamiin
            </p>
            <div class="mt-6 text-center">
              <p class="text-gray-600">- morgan</p>
            </div>
          </div>
        </div>
      </div>
      <div>
        <div class="flex justify-center items-center mt-5 p-4">
          <div class="max-w-md p-6 bg-white rounded-lg shadow-lg">
            <h2 class="text-2xl font-bold text-gray-800 text-center mb-4">Terima Kasih</h2>
            <p class="text-gray-600 text-center">
              Teruntuk teman-teman curhatku (wkwk), makasih ya ges sudah selalu mendengar keluh kesahku. Maaf suka bebal :-)
            </p>
            <div class="mt-6 text-center">
              <p class="text-gray-600">- morgan</p>
            </div>
          </div>
        </div>
      </div>
      <div>
        <div class="flex justify-center items-center mt-5 p-4">
          <div class="max-w-md p-6 bg-white rounded-lg shadow-lg">
            <h2 class="text-2xl font-bold text-gray-800 text-center mb-4">Plant care tips:</h2>
            <p class="text-gray-600 text-center">
                1. Light it up in so many ways<br>
                2. Hydrate and forget about it.<br>
                3. Keep it well fed.<br>

                // <br>
                
                1. Berikan cahaya dengan berbagai cara<br>
                2. Sirami dan lupakan sejenak.<br>
                3. Pastikan diberi nutrisi yang cukup.<br>
            </p>
            <div class="mt-6 text-center">
                <p class="text-gray-600">Happy Growing!</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <footer id="contact">
      <Footer />
    </footer>
  </div>
</template>

<style>
.bg-container {
  height: 100vh;
  width: 100vw;
  overflow: auto; /* Ensure content can scroll */
  /* background-color: black;  */
}
</style>

<script>
import YouTubeVideos from "@/components/YouTubeVideos.vue";
import BandLabEmbed from "@/components/BandLabEmbed.vue";
import Footer from "@/components/Footer.vue";

export default {
  components: {
    YouTubeVideos,
    BandLabEmbed,
    Footer,
  },
  data() {
    return {
      hidden: false,
      isModalVisible: false,
      selectedVideoUrl: '',
      videos: [
        { id: "4At0dI8xJa4" },
        { id: "Wz9BlivgSbo" },
        { id: "KG5fkBOLg4c" },
        { id: "-Zm_VqCsCCY" },
        { id: "15xQoUNMWVc" },
        { id: "4Sqw-GwACNI" },
        { id: "E2OZb9yknjU" },
        { id: "b3KM9OthMoA" },
        { id: "-W01JTUmr9s" },
        { id: "djzBGrzEWzI" },
        { id: "_CUD9lIzxBo" },
        { id: "80DxoS3t9vg" },
        { id: "KluIuQGYeM0" },
        { id: "pcrVyJj6CYk" },
      ],
      tracks: [
        { id: "77dde34a-1640-ef11-86c3-000d3a42581b" },
        // Add more BandLab track IDs as needed
      ],
    };
  },
  computed: {
    backgroundStyle() {
      return {
        backgroundImage: `url(${require('~/assets/images/plants.svg')})`,
        backgroundRepeat: 'no-repeat',
        backgroundPosition: 'center center',
        backgroundAttachment: 'fixed',
        backgroundSize: 'cover',
      };
    },
  },
  methods: {
    hideIt() {
      this.hidden = !this.hidden;
    },    
  },
  mounted() {
    // Force reactivity to ensure background image is applied
    this.$forceUpdate();
  },
};
</script>
