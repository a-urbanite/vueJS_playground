<template>
  <p v-if="fingers > 0">this hand has {{fingers}} fingers ✋</p>

  <p v-else>noooo, luck has run out! 😭</p>

  <button v-on:click="playKnifeGame()">play the knife game! 🔪</button>
  <button v-if="fingers === 0" v-on:click="magicRestore()">do some healy magic ✨</button>
</template>

<script>
  export default {
    data() {
      return {
        fingers: 5,
      }
    },

    methods: {
      playKnifeGame() {
        this.fingers--;
      },

      magicRestore() {
        this.fingers = 5
      }
    }
  }
</script>