<script lang="ts" setup>
defineProps({
  href: String,
  text: String,
  icon: String,
})
</script>

<template lang="pug">
a.flex.px-2.items-center.py-1.justify-baseline.no-under-line.text-white(class="hover:bg-gray-200 rounded-full" :href="href")
  span.mr-1.leading-none {{text}}
  span(:i="icon")
</template>
