<!-- global-bottom.vue -->
<template>
    <link href="https://fonts.googleapis.com/css2?family=Geo&family=Lato&display=swap" rel="stylesheet">  

  <footer v-if="$nav.currentLayout !== 'statement'" class="absolute bottom-0 left-0 right-0 p-2"><img src="./images/logo_final_transparent.png" width=2.5% /></footer>
  <footer v-if="$nav.currentLayout !== 'statement'" class="absolute bottom-0 left-100 right-0 p-2"><a href="https://bioinfo.guru" style="font-family: 'Geo', sans-serif; color:#9c51e0;">bioinfo.guru</a></footer>
  <footer
    v-if="$nav.currentLayout !== 'statement'"
    class="absolute bottom-0 left-220 right-0 p-2"
  >
    {{ $nav.currentPage }} / {{ $nav.total }}
  </footer>
</template>