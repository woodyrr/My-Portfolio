<template>
    <div class="sm:col-span-2 bg-green-100 border flex flex-col gap-3 py-2 px-3 justify-center items-start rounded-3xl">
        <img src="../assets/woodys-bitmoji.png" alt="" srcset="" class=" rounded-lg  max-w[800px] h-[96px] 2xl:h-[132px]" >
        <h1 class="font-semibold">
            Hello, my name's Woody Ramey.
            I am a highly motivated Front end developer who loves building the front end of websites and Web Applications that lead to the success of the overall product.
            when I am not coding, I usualy find myself in the kichen improving my baking skills or online reading webnovels.
            I'm open to Job opportunities where I can contribute, learn and grow. If you have a good opportunity that matches my skills then don't hesitate to contact me.
        
        </h1>
    </div>
    <div class=" bg-white flex items-center justify-center rounded-2xl">
        <div class="grid grid-cols-2 lg:grid-cols-3 gap-2 py-3 xl:py-0"> 
            <button class=" p-2 duration-200 font-semibold hover:bg-gray-200 border rounded-lg ">HTML</button>
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
    <a href="https://github.com/woodyrr" target="_blank" class=" bg-white flex items-center rounded-full sm:rounded-none justify-center sm:rounded-r-full sm:rounded-tr-full ">
        <i class="fa-brands fa-github p-2  text-[50px] sm:text-[130px] lg:text-[170px] xl:text-[200px] duration-300 hover:text-purple-600 "></i>
    </a>
    <a href="https://www.linkedin.com/in/woody-ramey-b84152267/" target="_blank" class="bg-white flex items-center rounded-full  justify-center sm:rounded-3xl">
        <i class="fa-brands fa-linkedin p-2 text-[50px] sm:text-[70px] lg:text-[100px] xl:text-[100px] duration-300 text-blue-600"></i>
    </a>
    <a :href="resume" alt="" srcset="" download class="flex justify-center items-center gap-2 bg-gray-200 rounded-xl">
        <i class="fa-regular fa-file text-[25px] xl:text-[40px]  duration-300 p-2"></i>
        <h3>download resume</h3>
    </a>
    <!-- <router-link :to="resume">
        <i class="fa-regular fa-file"></i>
    </router-link> -->
</template>
<script setup>
import resume from '../assets/WOODY-RAMEY.pdf'
import { RouterLink } from 'vue-router';
</script>