
<template>
  <EventHandling/>
  <ListRendering/>
  <Watchers/>
  <LifeCycleHooks/>
  <div class="flex border-4 border-red-500 flex-col rounded-xl justify-center shadow-2xl h-96  items-center bg-stone-600 w-3/4">
    <div class="text-cyan-400 h-auto text-4xl flex justify-center items-center p-4 mb-4 w-auto rounded-2xl hover:scale-125 bg-black">{{ fullName }}</div>
    <div class="flex flex-row justify-center items-center p-5">
      <label class="text-[#00FF00] text-2xl" for="">First name:  </label>
      <input type="text" placeholder="First Name " v-model.lazy="firstName" class="bg-black border w-auto shadow-2xl text-[#00FF00] border-red-500 rounded-xl h-11 p-5 ml-5">
      
    </div>
    <div class="flex flex-row justify-center items-center p-5 ">
      <label class="text-[#00FF00] text-2xl" for="">Last name:  </label>
      <input type="text" placeholder="Last Name " v-model="lastName" class="bg-black border w-auto shadow-2xl text-[#00FF00] border-red-500 rounded-xl h-11 p-5 mt-4 ml-5">

    </div>

  </div>

  
</template>

<script setup>
import EventHandling from './EventHandling.vue';
import ListRendering from './ListRendering.vue';
import Watchers from './Watchers.vue'
import LifeCycleHooks from './LifeCycleHooks.vue'; 
  import { ref , computed } from 'vue'

  let firstName = ref("")
  let lastName = ref("")

  let fullName = computed(()=>{
    return `${firstName.value} ${lastName.value}`
  })
    
</script>
<style scoped>

</style>
