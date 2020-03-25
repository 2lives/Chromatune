<template lang="pug">
table
    tr.row
        hexagon(v-for="i in 10" :key="i + 'row'" :colour="i % 2 > 0 ? 'navy-blue' : 'mint'")
    tr.odd-row
        hexagon(v-for="i in 11" :key="i + 'odd-row'" :colour="i % 2 > 0 ? 'copper' : 'other-copper'")

</template>
<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import Hexagon from './hexagon.vue';

@Component({
    components: {
        Hexagon
    }
})
export default class GridRow extends Vue {
    
}
</script>
<style scoped>
table {
    margin-top: -25px;
}
.row {
    display: flex
}

.odd-row {
    display: flex;
    margin-left: 50px;
    margin-top: -20px;
}
</style>