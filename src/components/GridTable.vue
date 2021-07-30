<template>
  <div class="grid-table">
    <div v-for="(th, index) in ths" :key="`th${index}`" class="th">{{th}}</div>
    <template v-for="(td, index) in tds" :key="`td${index}`">
      <div class="td">{{td.a}}</div>
      <div class="td">{{td.b}}</div>
      <div class="td">{{td.c}}</div>
    </template>
  </div>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  setup() {
    const ths = ['th1', 'th2', 'th3']
    const tds = [
      { a: 1, b: 2, c:3 },
      { a: 1, b: 2, c:3 },
      { a: 1, b: 2, c:3 },
      { a: 1, b: 2, c:3 },
    ]

    return {
      ths,
      tds
    }
  },
})
</script>

<style scoped>
.grid-table {
  display: grid;
  grid-template-columns: repeat(3, auto);
}
</style>
