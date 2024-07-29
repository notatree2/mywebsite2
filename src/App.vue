<script setup>
  import { ref } from "vue"
  const website = ref("https://tech-independence-journey.codeberg.page/")
  const old = ref("https://notatree2.github.io/mywebsite/")
  const github = ref("src\assets\images\github.png")
  

</script>

<template>
  <div class="rounded-lg bg-neutral-100 p-10 text-center overflow-hidden shadow-xl shadow-slate-300/3 mt-24 mr-48 ml-48">
    <div class="text-pretty text-slate-600 leading-relaxed">
      <p>Hello, and welcome to the placeholder frontpage for my new website! You can check out the source if you wish. You can also check out the old website, or a project called Tech Independence Journey! Very heavily inspired off a <a href="https://www.youtube.com/watch?v=UHciHtsuFnw" class="text-blue-500">tutorial</a> (though i tried to write the code by myself)</p>
        <div class=" grid columns-2 w-full rounded-xl p-5 font-medium">
          <button class=" border rounded-lg bg-slate-300 p-3"><a :href="old" target="_blank">Old Website</a></button>
          <button class=" p-3 border rounded-lg bg-blue-300"><a :href="website" target="_blank">Tech Independence Journey</a></button>
          
        </div>
        
      </div>
  
  
  </div>
</template>

<style scoped>

</style>
