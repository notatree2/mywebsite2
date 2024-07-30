<script setup>

  import { ref } from "vue"
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
    statian.value = "Did you know you click me?"
  } else if (status === 4) {
    statian.value = "Hmm... what do i put here lol"
  } else if (status === 5) {
    statian.value = "My ROBLOX username is Ifartedchicken, if you want you can check my profile out"
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
      statian.value = "Hmm... what do i put here lol"
    } else if (random === 5) {
      statian.value = "My ROBLOX username is Ifartedchicken, if you want you can check my profile out"
    } else if (random === 6) {
      statian.value = "The Lord is so cool (im a Christian)"
    } else if (random === 7) {
      statian.value = "Putting water on paper is not a good idea"
    } else {
      statian.value = "Ice is pretty cold ngl"
    }
  }
  

</script>

<template>
  <div class="rounded-lg bg-neutral-100 p-10 text-center overflow-hidden shadow-xl shadow-slate-300/3 mt-24 mr-48 ml-48">
    <div class="text-pretty text-slate-600 leading-relaxed">
      <p>Hello, and welcome to the placeholder frontpage for my new website! You can check out the source if you wish. You can also check out the old website, or a project called Tech Independence Journey! Very heavily inspired off a <a href="https://www.youtube.com/watch?v=UHciHtsuFnw" class="text-blue-500">tutorial</a> (though i tried to write the code by myself)</p>
        <div class=" grid columns-2 w-full rounded-xl p-5 font-medium">
          <button class=" border rounded-lg bg-slate-300 p-3 transition-colors hover:bg-slate-400 active:bg-slate-500"><a :href="old" target="_blank">Old Website</a></button>
          <button class=" p-3 border rounded-lg bg-blue-300 transition-colors hover:bg-blue-400 active:bg-blue-500"><a :href="website" target="_blank">Tech Independence Journey</a></button>
          
        </div>
        <p @click="changeme">{{statian}}</p>
      </div>
  
  
  </div>
</template>

<style scoped>

</style>
