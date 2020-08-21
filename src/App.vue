<template>
  <svg style="width:128px;height:128px" viewBox="0 0 24 24">
    <defs>
      <linearGradient id="gradient" x1="0" x2="0" y1="0" y2="1">
        <stop offset="0%" stop-color="#29B6F6"/>
        <stop offset="51%" stop-color="#039BE5"/>
        <stop offset="100%" stop-color="#0277BD"/>
      </linearGradient>
    </defs>
    <path fill="url(#gradient)" d="M12,17A2,2 0 0,0 14,15C14,13.89 13.1,13 12,13A2,2 0 0,0 10,15A2,2 0 0,0 12,17M18,8A2,2 0 0,1 20,10V20A2,2 0 0,1 18,22H6A2,2 0 0,1 4,20V10C4,8.89 4.9,8 6,8H7V6A5,5 0 0,1 12,1A5,5 0 0,1 17,6V8H18M12,3A3,3 0 0,0 9,6V8H15V6A3,3 0 0,0 12,3Z" />
  </svg>
  <PassphraseGenerator />
</template>

<script>
import PassphraseGenerator from './components/PassphraseGenerator.vue'

export default {
  name: 'App',
  components: {
    PassphraseGenerator
  }
}
</script>
