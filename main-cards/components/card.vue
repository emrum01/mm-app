<template lang="pug">
  .init
    v-card.card
      v-card-title(class="justify-center")
        div
          h3 テスト
      v-card-actions
        button.arrow
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
<style lang="scss" scoped>
.init {
}
.init ::v-deep .card {
  background: #ffbdbd;
  outline: none;
}
.card ::v-deep .arrow {
  width: 0px;
  border-color: #d9534f;
  border-style: solid;
  border-width: 30px;
  border-left-color: transparent;
  border-top-color: transparent;
  border-right-color: transparent;
  outline: none;
}
</style>
