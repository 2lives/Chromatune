<template lang="pug">
.body
  grid-row(v-for="i in 10" :key="i")
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import GridRow from './grid-row.vue';

@Component({
  components: {
    GridRow
  }
})

export default class Grid extends Vue {
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
