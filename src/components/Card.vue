<script setup>
const props = defineProps(['title', 'text', 'icon', 'color']);
var i;
if (props.icon.startsWith('fa')) {
  i = '<i class="' + props.icon + '"></i>'
} else i = '<div class="' + props.icon + '"></div>'
</script>

<template>
  <li class="card-round" v-html="i" v-bind:style="'--i-color: ' + props.color"></li>
</template>

<style lang="scss" scoped>
</style>