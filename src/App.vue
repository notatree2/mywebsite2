<script setup>


  import { ref, onMounted, computed } from "vue"
  import { useDark, useToggle } from '@vueuse/core';
  const isDark = ref(useDark())
  const website = ref("https://tech-independence-journey.codeberg.page/")
  const old = ref("https://notatree2.github.io/mywebsite/")
  const source = ref("https://github.com/notatree2/mywebsite2")
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
    statian.value = "The internet is pretty cool"
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
      statian.value = "The internet is pretty cool"
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
<div class="place-content-center h-screen dark:bg-slate-700 z-0">
  <div class="rounded-lg bg-neutral-100 p-10 text-center overflow-hidden shadow-xl shadow-slate-300/3 mr-48 ml-48 dark:bg-slate-800 z-10">
    
    <div class="text-pretty text-slate-600 leading-relaxed dark:text-slate-400 tracking-normal ">
      <h1 class="font-bold text-3xl p-3 font-sans ">Hello, i am notacupofmilk.</h1>
      <p>I am a Christian, gamer, and i like the internet. This website right now is a placeholder for whats to come. The source code can be found <a :href="source" class="font-bold text-blue-400 hover:text-blue-500 transition transition-all active:text-blue-600">here.</a>  Very heavily inspired off a <a href="https://www.youtube.com/watch?v=UHciHtsuFnw" class="text-blue-500">tutorial</a> (though i tried to write the code by myself)</p>
      <br>
        <div class="grid grid-cols-2 w-full rounded-xl p-5 font-medium gap-2 ">
          <a :href="old" target="_blank"><button class="  w-full border rounded-lg bg-slate-300 p-3 transition-colors hover:bg-slate-400 active:bg-slate-500 dark:bg-slate-600">Old Website</button></a>
          <a :href="website" target="_blank"><button class=" w-full p-3 border rounded-lg bg-blue-300 transition-colors hover:bg-blue-400 active:bg-blue-500 dark:text-slate-900">Tech Independence Journey</button></a>
          
        </div>
        <p @click="changeme" class="animation animate-bounce duration-400">{{statian}}</p>
        <br>
        <div class="border border-neutral-100  dark:border-slate-800 p-2 group mr-96 ml-96">
          
          <input type="checkbox" v-model="isDark" class="rounded-lg focus:ring-1 focus:ring-slate-400 transition transition-all focus:ring-offset-2 "> <label class="opacity-0 group-hover:opacity-100 transition transition-opacity font-semibold">Enable Dark mode</label>
        </div>
        
      </div>
  
  
  </div>
</div>
</template>

<style scoped>

</style>
