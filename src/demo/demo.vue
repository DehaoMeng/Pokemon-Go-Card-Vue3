<script setup lang="ts">
import ImagePoke from "@/components/Image-Poke.vue";
import {ref} from "vue";
const path = ref(new URL('@/assets/img.png', import.meta.url))
const width = ref('10vw')
const height = ref('20vh')
const pop = ref('true')
</script>

<template>
  <div>
    <div>
      <ImagePoke :path="path"/>
      单一实例
    </div>
    <div>
    <ImagePoke :path="path" :width="width" :height="height"/>
      自定义宽高
    </div>
    <div>
      <ImagePoke :path="path" :width="width" :height="height" :pop="pop"/>
      可点击放大
    </div>
  </div>
</template>

<style scoped>

</style>
