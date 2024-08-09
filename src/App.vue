<script setup>


  import { ref, onMounted, computed } from "vue"
  import { useDark, useToggle } from '@vueuse/core';
  const isDark = ref(useDark())
  const website = ref("https://tech-independence-journey.codeberg.page/")
  const old = ref("https://notatree2.github.io/mywebsite/")
  const github = ref("src\assets\images\github.png")
  const statian = ref("")
  // ---------------------------------------------------------------
  
  const status = Math.floor(Math.random() * 8)
  if (status === 1) {
    statian.value = "1+1=2"
  } else if (status === 2) {
    statian.value = "Do you like music?"
  } else if (status === 3) {
    statian.value = "Did you know you can click me?"
  } else if (status === 4) {
    statian.value = "People say i am a furry... and at this point i cant deny it anymore whether i like it or not"
  } else if (status === 5) {
    statian.value = "Counter Strike is pretty cool ngl"
  } else if (status === 6) {
    statian.value = "The Lord is so cool (im a Christian)"
  } else if (status === 7) {
    statian.value = "Putting water on paper is not a good idea"
  } else {
    statian.value = "Ice is pretty cold ngl"
  }



  const changeme = () => {
    const random = Math.floor(Math.random() * 8)
    if (random === 1) {
      statian.value = "2+2=4"
    } else if (random === 2) {
      statian.value = "Do you like music?"
    } else if (random === 3) {
      statian.value = "What you doing?"
    } else if (random === 4) {
      statian.value = "People say i am a furry... and at this point i cant deny it anymore whether i like it or not"
    } else if (random === 5) {
      statian.value = "Counter Strike is pretty cool ngl"
    } else if (random === 6) {
      statian.value = "The Lord is so cool (im a Christian)"
    } else if (random === 7) {
      statian.value = "Putting water on paper is not a good idea"
    } else {
      statian.value = "Ice is pretty cold ngl"
    }
  }
  onMounted(() => {
    console.log("finished the initial rendering and created DOM nodes")
  })

</script>

<template>
<div class="place-content-center h-screen dark:bg-slate z-0">
  <div class="rounded-lg bg-neutral-100 p-10 text-center overflow-hidden shadow-xl shadow-slate-300/3 mr-48 ml-48 dark:bg-slate-800 z-10">
    <div class="text-pretty text-slate-600 leading-relaxed dark:text-slate-400">
      <p>Hello, and welcome to the placeholder frontpage for my new website! You can check out the source if you wish. You can also check out the old website, or a project called Tech Independence Journey! Very heavily inspired off a <a href="https://www.youtube.com/watch?v=UHciHtsuFnw" class="text-blue-500">tutorial</a> (though i tried to write the code by myself)</p>
        <div class=" grid rows-2 w-full rounded-xl p-5 font-medium gap-2">
          <a :href="old" target="_blank"><button class="  w-full border rounded-lg bg-slate-300 p-3 transition-colors hover:bg-slate-400 active:bg-slate-500 dark:bg-slate-600">Old Website</button></a>
          <a :href="website" target="_blank"><button class=" w-full p-3 border rounded-lg bg-blue-300 transition-colors hover:bg-blue-400 active:bg-blue-500 dark:text-slate-900">Tech Independence Journey</button></a>
          
        </div>
        <p @click="changeme" class="animation animate-bounce duration-400">{{statian}}</p>
        <input type="checkbox" v-model="isDark">
      </div>
  
  
  </div>
</div>
</template>

<style scoped>

</style>
