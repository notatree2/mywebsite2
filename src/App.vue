<script setup>


  import { ref, onMounted, computed } from "vue"
  import { useDark, useToggle } from '@vueuse/core';
  import buttons from "./components/buttons.vue"
  import dropdown from "./components/dropdownmenutest.vue"
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
      statian.value = "Xiao Xiao is a stickman animation series from like the early or late 2000s idk"
    } else if (random === 2) {
      statian.value = "Do you like music?"
    } else if (random === 3) {
      statian.value = "What you doing?"
    } else if (random === 4) {
      statian.value = "The internet is pretty cool"
    } else if (random === 5) {
      statian.value = "STICK WAR"
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
  
<div class="place-content-center h-screen dark:to-slate-700 dark:from-slate-800 z-0 bg-gradient-to-tl">
  
  <div class="rounded-lg bg-neutral-100 p-10 text-center overflow-hidden shadow-xl shadow-slate-300/3 mr-48 ml-48 dark:bg-slate-800 z-10">
    
    <div class="text-pretty text-slate-600 leading-relaxed dark:text-slate-400 tracking-normal ">
      <h1 class="font-bold text-3xl p-3 font-sans ">Hello, i am .</h1>
      <p> Can i call myself notacupofmilk anymore? I don't think i can, I feel as if i have dropped that name. And for good reason, I did so to save my life. I was probably going to kill myself if I didn't, for it had only been about a week. Had it not been for Area 51's collapse i would still be around, but I dont want to use that to convince people. <br>I am isolated and lonely, and I only talk to my parents. I have found it cringe to express my feelings, but that's irrational. I would like to come back, but for the sake of my morals and sanity, i dont think i can. I would like to thank you all for being my friend, and spending time with me. I really do appreciate it. <a :href="source" class="font-bold text-blue-400 hover:text-blue-500 transition transition-all active:text-blue-600">Github found here,</a> and my inspiration.<a href="https://www.youtube.com/watch?v=UHciHtsuFnw" class="text-blue-500">tutorial</a> (though i tried to write the code by myself)</p>
      <br>
      <div class="border border-slate-200 dark:border-slate-700 mr-24 ml-24"></div>
      <buttons />
        <!-- 
        <p @click="changeme" class="animation animate-bounce duration-1000">{{statian}}</p>
        <br>
        <div class="border border-neutral-100  dark:border-slate-800 p-2 group mr-96 ml-96">
          -->
          <input type="checkbox" v-model="isDark" class="rounded-lg focus:ring-1 focus:ring-slate-400 transition transition-all focus:ring-offset-2 cursor-pointer "> <label  class="opacity-0 group-hover:opacity-100 transition transition-opacity font-semibold ">Enable Dark mode</label>
        
        </div>
        
      </div>
  
  
  </div>
  <!-- <dropdown /> -->

</template>

<style scoped>

</style>
