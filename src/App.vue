<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import { vDrag } from './directives/dragDirective';
import { vScale } from './directives/scaleDirective';
</script>

<template>
<div class="box">
  <HelloWorld v-scale v-drag="{limit: 0.5, classList:['draging'], dragArea:'parent'}"/>
  <!-- <HelloWorld v-drag="{limit: 1, classList:['draging'], dragArea:'parent'}"/> -->
  <!-- <HelloWorld v-drag="{limit: 1, classList:['draging']}"/> -->
</div>
</template>

<style>
*{
  margin: 0;
  padding: 0;
}
.box{
  width: 700px;
  height: 500px;
  border: solid rgb(138, 133, 133) 10px;
  position: absolute;
  margin: 0 auto;
  left: 50px;
  top: 50px;
}
.draging{
  opacity: 0.5;
  cursor:grab;
}
</style>
