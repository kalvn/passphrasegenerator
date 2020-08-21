<template>
  <div>
    <div class="passphrase">{{ passphrase }}</div>
    <button @click="generate()" class="is-with-gradient">générer une nouvelle phrase de passe</button>
    <div class="filters">
      <div class="filter">
        <label for="number-of-words">number of words</label>
        <input type="number" id="number-of-words" v-model="numberOfWords">
      </div>

    </div>
  </div>
</template>

<script>
import words from '../words';

export default {
  name: 'PassphraseGenerator',
  mounted: function () {
    this.generate();
  },
  data() {
    return {
      passphrase: '',
      numberOfWords: 4
    }
  },
  methods: {
    generate: function () {
      const length = words.length;
      let result = [];

      for (let i = 0; i < this.numberOfWords; i++) {
        result.push(words[Math.floor(Math.random() * length)]);
      }

      this.passphrase = result.join(' ');
    }
  }
}
</script>
