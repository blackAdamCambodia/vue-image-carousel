<script setup>
import {ref, reactive} from "vue";
const fullImage= ref('https://images.unsplash.com/photo-1688224196207-7e3be84f71db?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwxNjZ8fHxlbnwwfHx8fHw%3D&auto=format&fit=crop&w=500&q=60')
const images = [
  {
    thumb: "https://images.unsplash.com/photo-1688224196207-7e3be84f71db?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwxNjZ8fHxlbnwwfHx8fHw%3D&auto=format&fit=crop&w=500&q=60",
    full: "https://images.unsplash.com/photo-1688224196207-7e3be84f71db?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHwxNjZ8fHxlbnwwfHx8fHw%3D&auto=format&fit=crop&w=500&q=60"
  },
  {
    thumb: "https://images.unsplash.com/photo-1668183261803-e8f2fb7622dd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxjb2xsZWN0aW9uLXBhZ2V8M3w5OTl8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60",
    full: "https://images.unsplash.com/photo-1668183261803-e8f2fb7622dd?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxjb2xsZWN0aW9uLXBhZ2V8M3w5OTl8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=500&q=60"
  },
  {
    thumb: "https://images.unsplash.com/photo-1671017623387-4f48edaf5ce3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxjb2xsZWN0aW9uLXBhZ2V8MnwxNDY2NDc3fHxlbnwwfHx8fHw%3D&auto=format&fit=crop&w=500&q=60",
    full: "https://images.unsplash.com/photo-1671017623387-4f48edaf5ce3?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxjb2xsZWN0aW9uLXBhZ2V8MnwxNDY2NDc3fHxlbnwwfHx8fHw%3D&auto=format&fit=crop&w=500&q=60"
  },
  {
    thumb: "https://images.unsplash.com/photo-1669940812749-0a0fa4b92ba4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80",
    full: "https://images.unsplash.com/photo-1669940812749-0a0fa4b92ba4?ixlib=rb-4.0.3&ixid=M3wxMjA3fDF8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1740&q=80"
  }
]
function setImage(image) {
  fullImage.value = image.full
}
</script>

<template>
   <section class="container mx-auto flex items-center flex-col">
        <h1 class="text-center text-2xl py-10">Events & Reactivity</h1>
        <div class="">
            <div class="flex space-x-2">
                <img @click="setImage(image)" class="cursor-pointer thumb " :src="image.thumb" v-for="image in images" :key="image.thumb" alt="">
               
            </div>
            <div class="mt-10">
                <img class="cursor-pointer fullImage w-full" :src="fullImage" alt="">
            </div>
        </div>
    </section>
</template>

<style scoped>
  .thumb {
    width: 300px ;
    height: 250px;
  }
  .fullImage {
    width: 100%;
    height: 800px;
  }

</style>

