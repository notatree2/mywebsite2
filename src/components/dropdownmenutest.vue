<script>
import { ref } from "vue"
const isHidden1 = ref(true) // if hidden1 false, dropdown menu revealed
const isHidden2 = ref(false) // if hidden2 false, dropdown menu not revealed
const sethidval = () => {
    if (isHidden1 === true) {
        isHidden1.value = false
        isHidden2.value = true
    } else {
        isHidden1.value = true 
        isHidden2.value = false
    }


}

</script>

<template>
    
    <div class="relative">
        <div class=" border-solid border-gray-400 border-3 py-2 px-3 rounded cursor-pointer bg-white font-bold w-[200px] shadow-sm" @click="sethidval">
            Options
            
        </div>
        <!--btn-->
        <div :class="{hidden: isHidden1 }">
            <div class="rounded border-[1px] border-gray-500 bg-white absolute top-[50px] w-[400px] shadow-lg">
                <div class="transition transition-all hover:bg-slate-500 cursor-pointer p-3">More</div>
                <div class="transition transition-all hover:bg-slate-500 cursor-pointer p-3">Licensing</div>
                <div class="transition transition-all hover:bg-slate-500 cursor-pointer p-3">Appearance</div>
                <div class="transition transition-all hover:bg-slate-500 cursor-pointer p-3">Privacy</div>
            </div>
        </div>
        <!--btn-->
    </div>
</template>

