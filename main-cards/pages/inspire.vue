<template lang="pug">
  .pt-0
    v-card(:loading="loading"
      class="mx-auto my-12"
      max-width="374")
      v-card-text
        p {{name}}
      v-card-action
        v-btn
    card
</template>
<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
import card from '~/components/card.vue'

@Component({
  layout: 'default',
  components: { card },
  head() {
    return {
      title: 'test',
    }
  },
})
export default class Top extends Vue {
  public name: string = 'taro'
  public age: number = 24
  public country: string = '日本'
  public score: number = 55
  get triple() {
    return this.score * 3
  }
}
</script>
<style lang="scss" scoped></style>
