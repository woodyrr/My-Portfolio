<template>
<main class="grid grid-cols-1 sm:grid-cols-2 px-[8%] md:px-[10%] lg:px-[12%]  xl:px-[20%] gap-5">
    <section v-for="item in data">
        
            <div class="p-4 rounded-md bg-[#09200685] text-black ">
                <div class="bg-transparent overflow-hidden relative w-full space-y-5 cursor-pointer">
                    <div class="relative h-full w-full">
                            <div class="h-full w-full relative bg-gray-50 dark:bg-[#09090B] rounded-xl" style="transform: none;">
                                <img alt="image" loading="lazy" decoding="async" data-nimg="1" class="sm:h-[200px] md:h-[200px] lg:h-[250px] xl:h-[300px] w-full object-cover hover:opacity-0 rounded-lg" style="color:transparent; opacity:0.9;"  :src="item.image" >
                            </div>
                            
                            <div  class="absolute pt-[42%] top-0 left-0 pl-4 z-40 h-full w-full opacity-0 duration-500 hover:pt-[28%] hover:opacity-100 bg-[#8d968fe0] rounded-sm" >
                                <div class="flex flex-col gap-1 md:gap-2 lg:gap-3">

                                    <h1 class="text-xl lg:text-2xl font-bold text-white  ">{{ item.name }}</h1>
                                    <div class="flex items-center gap-1">
                                        <div v-if="item.tech1 == 'Vuejs'">
                                            <i class="fa-brands fa-vuejs text-2xl md:text-3xl xl:text-4xl text-green-600"></i>
                                        </div>
                                        <div v-if="item.tech4 == 'Javascript'">
                                            <i class="fa-brands fa-js text-2xl md:text-3xl xl:text-4xl text-yellow-500"></i>
                                        </div>
                                        <div v-if="item.tech2 == 'CSS'">
                                            <i class="fa-brands fa-css3-alt text-2xl md:text-3xl xl:text-4xl"></i>
                                        </div>
                                        <div v-if="item.tech3 == 'Tailwindcss'">
                                            <svg stroke="currentColor" fill="currentColor" stroke-width="0" role="img" viewBox="0 0 24 24" class="h-6 w-6 md:w-8 md:h-8  xl:w-10 xl:h-10 mx-auto text-blue-400" height="1em" width="1em" xmlns="http://www.w3.org/2000/svg"><path d="M12.001,4.8c-3.2,0-5.2,1.6-6,4.8c1.2-1.6,2.6-2.2,4.2-1.8c0.913,0.228,1.565,0.89,2.288,1.624 C13.666,10.618,15.027,12,18.001,12c3.2,0,5.2-1.6,6-4.8c-1.2,1.6-2.6,2.2-4.2,1.8c-0.913-0.228-1.565-0.89-2.288-1.624 C16.337,6.182,14.976,4.8,12.001,4.8z M6.001,12c-3.2,0-5.2,1.6-6,4.8c1.2-1.6,2.6-2.2,4.2-1.8c0.913,0.228,1.565,0.89,2.288,1.624 c1.177,1.194,2.538,2.576,5.512,2.576c3.2,0,5.2-1.6,6-4.8c-1.2,1.6-2.6,2.2-4.2,1.8c-0.913-0.228-1.565-0.89-2.288-1.624 C10.337,13.382,8.976,12,6.001,12z"></path></svg>
                                        </div>
                                        <div v-if="item.tech4 == 'Firebase'">
                                            <svg  xmlns="http://www.w3.org/2000/svg"  width="1em" height="1em" viewBox="0 0 48 48"class="w-8 h-8 xl:w-10 xl:h-10 mx-auto" >
                                                <path fill="#ff8f00" d="M8,37L23.234,8.436c0.321-0.602,1.189-0.591,1.494,0.02L30,19L8,37z"></path><path fill="#ffa000" d="M8,36.992l5.546-34.199c0.145-0.895,1.347-1.089,1.767-0.285L26,22.992L8,36.992z"></path><path fill="#ff6f00" d="M8.008 36.986L8.208 36.829 25.737 22.488 20.793 13.012z"></path><path fill="#ffc400" d="M8,37l26.666-25.713c0.559-0.539,1.492-0.221,1.606,0.547L40,37l-15,8.743 c-0.609,0.342-1.352,0.342-1.961,0L8,37z"></path>
                                            </svg>
                                        </div>
                                    </div>
                                    <div class="flex gap-4 text-lg  lg:text-3xl items-center">
                                        <a :href="item.website" target="_blank" placeholder="website">
                                            <i class="fa-solid fa-globe"></i>
                                        </a>
                                        <a :href="item.github">
                                            <i class="fa-brands fa-github"></i>
                                        </a>
                                    </div>
                                    
                                </div> 
                            </div>
                    </div>
                </div>
            </div>
    </section>
    
</main>
</template>

<script setup>
import { ref } from 'vue'
import recipes from '../images/recipes-two-opal.vercel.app_home (1).png'
import threeb from '../images/threeb.vercel.app_ (1).png'
import Takes from '../images/best-takes.vercel.app_.png'
import Soleilla from '../images/woodyrr.github.io_Soleilla_.png'
import random from '../images/woodyrr.github.io_random-quotes_.png'

let data = [
{
        "id": 0,
        "name": "Voting App",
        "image": Takes,
        "description": "",
        "tech1": "Vuejs",
        "tech3": "Tailwindcss",
        "tech4": "Firebase",
        "website": "https://recipes-sigma-livid.vercel.app/",
        "github": "https://github.com/woodyrr/recipes"
        
    },
    {
        "id": 1,
        "name": "Recipes App",
        "image": recipes,
        "description": "This is recipe website that uses the meal DB API with a nice responsive user interface. It uses the mealdb api and googles firebase on the backend. This site provides auth and uses the firestore for data management. This was originaly for a front-end challenge on devChallenges.io, but I changed the original design a bit and connected a backend to it.",
        "tech1": "Vuejs",
        "tech3": "Tailwindcss",
        "tech4": "Firebase",
        "website": "https://recipes-sigma-livid.vercel.app/",
        "github": "https://github.com/woodyrr/recipes"
        
    },
    {
        "id": 2,
        "name": "E-commerce App",
        "image": Soleilla,
        "description": "An E-commerse application for buying candle, lotion  and tea products. This project has a special place in my heart because I designed it as the project went on.",
        "tech1": "html",
        "tech2": "CSS",
        "tech3": "Tailwindcss",
        "tech4": "Javascript",
        "website": "https://woodyrr.github.io/Soleilla/",
        "github": "https://github.com/woodyrr/Soleilla/tree/main2"
        
    },
    // {
    //     "id": 3,
    //     "name": "Anime App",
    //     "image": threeb,
    //     "description": "Anime/manga website where user can search for their favorite series to add and save their reading/watching status for next time. This site uses an anime api and taught me how to use use vuejs, Locale storage and apis.",
    //     "tech1": "Vuejs",
    //     "tech2": "CSS",
    //     "tech3": "Tailwindcss",
    //     "tech4": "Javascript",
    //     "website": "https://threeb.vercel.app/",
    //     "github": "https://github.com/woodyrr/TWB"
        
    // },
    
    // {
    //     "id": 4,
    //     "name": "Random-Quotes",
    //     "image": random,
    //     "description": "This website was a challenge assigned from devChallenges.io, the site uses an api and made responsive with options to toggle and copy quotes to keyboard.",
    //     "tech1": "html",
    //     "tech2": "CSS",
    //     "tech3": "Tailwindcss",
    //     "tech4": "Javascript",
    //     "website": "https://woodyrr.github.io/random-quotes/",
    //     "github": "https://github.com/woodyrr/random-quotes"
        
    // }
    // {
    //     "id": 5,
    //     "name": "Simple-homepage",
    //     "image": "images/woodyrr.github.io_simple-homepage_.png",
    //     "description": "Just a simple responsive home page With a light and dark mode option",
    //     "tech1": "html",
    //     "tech2": "CSS",
    //     "tech3": "Tailwindcss",
    //     "tech4": "Javascript",
    //     "website": "https://woodyrr.github.io/simple-homepage/",
    //     "github": "https://github.com/woodyrr/simple-homepage"
        
    // }
]

</script>

<style>
/* .content:hover .stuff {
  display: block;
  opacity: 1;
  transform:none;
} */

</style>