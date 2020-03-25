<template lang="pug">
div 
    .hexagon(:class="colour")
</template>
<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

@Component
export default class Hexagon extends Vue {
@Prop({type: String, required: false, default: 'red'}) colour!: string

mounted () {
    console.log(this.colour, 'colour')
}
}
</script>
<style scoped>
.hexagon {
    border: 1px solid #fff;
    height: 100px;
    width: 100px;
    clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
}
.navy-blue {
    background-color: #00203F;
}
.mint {
    background-color: #ADEFD1;
}
.copper {
    background-color: #B1624E;
}
.other-copper {
    background-color: #5CC8D7;
}
</style>