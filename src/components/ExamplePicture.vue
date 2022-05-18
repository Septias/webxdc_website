<script lang="ts" setup>
defineProps({
  image: String,
  text: String,
  href: String,
})
</script>

<template lang="pug">
a.picture.m-2.border-box.border.rounded-xl.flex.flex-col(class="width-1/3 hover:border-gray-200" :href="href")
    img.rounded-t-xl.border-bottom.flex-grow(:src="image" class="w-full")
    div.p-2 {{text}}
</template>

<style>
.picture{
  padding: 2px;
  background: #181a1b;
  border-color: #181a1b;
}
</style>
