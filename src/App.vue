<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref } from 'vue';
import about from './components/About.vue'
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


</script>

<template>
  <section class="py-10 flex flex-col gap-10 w-full">
    <div class="flex flex-col-reverse gap-6 sm:gap-0 sm:flex-row justify-between px-[5%] items-center">
      <h2 class="text-[20px]">WR</h2>
      <header class="flex justify-center gap-4 bg-gray-200 px-5 py-3 rounded-full items-center">
        <button class="px-3 py-1 rounded-xl duration-500 " :style="{ backgroundColor: buttons[0].backgroundColor}" @click="toggleBackgroundColor(0)">About</button>
        <button class="px-3 py-1 rounded-xl duration-500" :style="{ backgroundColor: buttons[1].backgroundColor}" @click="toggleBackgroundColor(1)">Projects</button>
        <button class="px-3 py-1 rounded-xl duration-500" :style="{ backgroundColor: buttons[2].backgroundColor}" @click="toggleBackgroundColor(2)">Contact</button>
      </header>
      <button id="light/dark" class="flex gap-2 bg-gray-300 px-4 py-2 rounded-xl">
          <i class="fa-solid fa-moon"></i>
          <i class="fa-regular fa-sun"></i>
      </button>
    </div>

    <section class="grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-4 gap-3 px-[4%] sm:px-[12%] w-full">
      <!-- <div class="bg-gray-200 flex justify-center items-center">
        <img src="./assets/woodys-bitmoji.png" alt="" srcset="">
      </div> -->
      <!-- <div class="">
        <img src="./assets/hey.png" alt="" srcset="" class="border rounded-lg  max-w[800px] h-[96px]" >
      </div> -->
      <div class="sm:col-span-2 bg-green-100 border flex flex-col gap-3 py-2 px-3 justify-center items-start rounded-3xl">
        <img src="./assets/woodys-bitmoji.png" alt="" srcset="" class=" rounded-lg  max-w[800px] h-[96px] 2xl:h-[132px]" >
        <h1 class="font-semibold">
            Hello, my name's Woody Ramey.
            I am a highly motivated Front end developer who loves building the front end of websites and Web Applications that lead to the success of the overall product.
            when I am not coding, I usualy find myself in the kichen improving my baking skills or online reading webnovels.
            
            
            when I am not coding, I usualy find myself in the kichen improving my baking skills or online reading webnovels.
            when I am not coding, I usualy find myself in the kichen improving my baking skills or online reading webnovels.
        </h1>
      </div>
      <div class=" bg-white flex items-center justify-center rounded-2xl">
        <div class="grid grid-cols-2 lg:grid-cols-3 gap-2 py-3 xl:py-0"> 
          <button class=" p-2 duration-200 font-semibold hover:bg-gray-200 border rounded-lg">HTML</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-yellow-200 border rounded-lg">Javascript</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-green-200 border rounded-lg">VueJS</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-blue-600 border rounded-lg">CSS</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-blue-200 border rounded-lg">Python</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-yellow-200 border rounded-lg col-span-2">Firebase database</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-blue-200 border rounded-lg">Tailwind</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-green-200 border rounded-lg">Git</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-black border rounded-lg hover:text-white">Github</button>
          <button class=" p-2 duration-200 font-semibold hover:bg-yellow-200 border rounded-lg">Nodejs</button>
        </div>
        
        
        
      </div>
      <!-- <div class=""> -->
        <a href="https://github.com/woodyrr" target="_blank" class="bg-white flex items-center rounded-full sm:rounded-none justify-center sm:rounded-r-full sm:rounded-tr-full ">
          <i class="fa-brands fa-github p-2 text-4xl text-[50px] sm:text-[130px] lg:text-[170px] xl:text-[200px] duration-300 hover:text-purple-600 "></i>
        </a>
      <!-- </div> -->
      <!-- <div class="bg-gray-300">
        <about />
      </div> -->
      
      
    </section>

    
    
  </section>

  <!-- <RouterView /> -->
</template>


