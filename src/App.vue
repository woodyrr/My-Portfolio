<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue';
import projects from './components/Projects.vue'
import abouts from './components/About.vue'
import contacts from './components/Contact.vue'
// let btn1 = document.querySelector(".btn1")
// function colorChange () {
//   btn1.b
// }
const buttons = ref([
  { backgroundColor: '' }, // Set the initial background color for the first button
  { backgroundColor: '' },
  { backgroundColor: '' }
]);

const activeButtonIndex = ref(0);
const toggleBackgroundColor = (index) => {
  if (index !== activeButtonIndex.value) {
    // Reset the background color of the previously active button
    buttons.value[activeButtonIndex.value].backgroundColor = '';

    // Set the new active button index
    activeButtonIndex.value = index;

    // Set the background color of the clicked button
    buttons.value[index].backgroundColor = '#fff';
  }
};
let project = ref(false)
let about = ref(true)
let contact = ref(false)
// const proj = () =>{
//   contact = true
//   about = false
//   contact = false
//   console.log("hey")
// }
// let abo = function(){
//   project = false
//   contact = false

// }
// const conta = function(){
//   project = false
//   about = false
// }


</script>

<template>
  <section class="py-10 flex flex-col gap-10 w-full font-semibold">
    <div class="flex flex-col-reverse gap-6 sm:gap-0 sm:flex-row justify-between px-[5%] items-center">
      <h2 class="text-[20px]">WR</h2>
      <header class="flex justify-center gap-4 bg-gray-200 px-5 py-3 rounded-full items-center">
        <button class="px-3 py-1 rounded-xl duration-500 hover:text-gray-400 " :style="{ backgroundColor: buttons[0].backgroundColor}" @click="toggleBackgroundColor(0), about = true, project = false, contact = false">About</button>
        <button class="px-3 py-1 rounded-xl duration-500 hover:text-gray-400 " :style="{ backgroundColor: buttons[1].backgroundColor}" @click="toggleBackgroundColor(1), project = true, about = false, contact = false">Projects</button>
        <button class="px-3 py-1 rounded-xl duration-500 hover:text-gray-400 " :style="{ backgroundColor: buttons[2].backgroundColor}" @click="toggleBackgroundColor(2), contact = true, project = false, about = false">Contact</button>
      </header>
      <!-- <button id="light/dark" class="flex gap-2 bg-gray-300 px-4 py-2 rounded-xl">
          <i class="fa-solid fa-moon"></i>
          <i class="fa-regular fa-sun"></i>
      </button> -->
      <h2 class="text-[17px]">Developer</h2>
    </div>
    <section v-if="project" class="flex flex-col gap-16">
      <projects />
    </section>
    <section v-else-if="contact" class="">
      <contacts/>
    </section>
    <section v-else-if="about" class="grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-4 gap-3 px-[4%] sm:px-[12%] w-full">
      <abouts />
    </section>

    
    
    
  </section>

  <!-- <RouterView /> -->
</template>
<style>
/* img{
    image-rendering: -webkit-optimize-contrast;
    object-fit: cover;
    
} */
</style>

