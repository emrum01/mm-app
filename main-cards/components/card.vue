<template lang="pug">
  v-card
    button(class="bg-purple-600 hover:bg-purple-700 focus:outline-none focus:ring-2 focus:ring-purple-600 focus:ring-opacity-50 ...")
</template>
<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'

@Component
export default class index extends Vue {
  public name: string = 'taro'
  public age: number = 24
  public country: string = '日本'
  public score: number = 55
  get triple() {
    return this.score * 3
  }
}
</script>
<style></style>
