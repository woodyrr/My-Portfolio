<template>
<main v-for="item in data" class="">
    <section class="flex flex-col lg:flex-row gap-3 px-[4%] sm:px-[12%] w-full bg-gray-200 md:bg-transparent py-3 ">
        <!-- <div class="flex items-center justify-center"> -->
        <img :src='item.image' alt="" class=" rounded-2xl border border-[rgba(20, 183, 224, 0.8)] w-full lg:w-[500px] xl:w-[450px]">
        <!-- </div> -->
        
        <div class="flex flex-col gap-4 ">
            <div class="text-[24px] font-bold text-center ">{{ item.name }}</div>
            <div class="bg-white sm:col-span-1 p-5 border rounded-3xl xl text-[16px] drop-shadow-xl">{{item.description}}</div>

            <div class="grid grid-cols-2 gap-1">
                <div class=" flex flex-col px-2 xl:px-[30%] rounded-2xl bg-gray-300 border">
                    <div class="flex gap-3 flex-col py-1 2xl:text-center">
                        <div class=" p-2 duration-200 font-semibold bg-green-100 border rounded-lg ">
                            {{ item.tech1 }}
                        </div>
                        <div v-if="item.tech2 " class=" p-2 duration-200 font-semibold bg-green-100 border rounded-lg">
                            {{ item.tech2 }}
                        </div>
                        <div class=" p-2 duration-200 font-semibold bg-green-100 border rounded-lg">
                            {{ item.tech3 }}
                        </div>
                        <div class=" p-2 duration-200 font-semibold bg-green-100 border rounded-lg">
                            {{ item.tech4 }}
                        </div>
                        
                    </div>
                    
                </div>
                <div class="bg-gray-200 rounded-2xl flex flex-col w-full justify-center gap-2 text-[20px] px-[10%]">
                    <a :href="item.website" target="_blank" class=" p-2 site flex items-center gap-1 rounded-lg bg-white justify-center"> 
                        <div>web</div>
                        <i class="fa-solid fa-arrow-trend-up"></i>
                    </a>
                    <a :href="item.github" target="_blank" class=" p-2 site flex items-center gap-1 rounded-lg bg-white justify-center"> 
                        <div>github</div>
                        <i class="fa-brands fa-github"></i>
                    </a>
                </div>
            </div>

            <!-- <img src="../assets/recipes-two-opal.vercel.app_home (1).png" alt="" srcset=""> -->
        </div>
        
        <!-- <div class="bg-white  p-5 border rounded-3xl">{{item.description}}</div> -->
    </section>
    
    <!-- <img :src=" item.image" alt="" class=" rounded-2xl border border-[rgba(20, 183, 224, 0.8)] max-w[800px] h-[96px] 2xl:h-[132px]"> -->
    
</main>
</template>

<script setup>
import recipes from '../images/recipes-two-opal.vercel.app_home (1).png'
import threeb from '../images/threeb.vercel.app_ (1).png'
import Takes from '../images/best-takes.vercel.app_.png'
import Soleilla from '../images/woodyrr.github.io_Soleilla_.png'
import random from '../images/woodyrr.github.io_random-quotes_.png'

let data = [
    {
        "id": 0,
        "name": "Best-Takes",
        "image": Takes,
        "description": "Voting app",
        "tech1": "Vuejs",
        "tech3": "Tailwindcss",
        "tech4": "Firebase",
        "website": "https://best-takes.vercel.app/",
        "github": "https://github.com/woodyrr/BestTakes"
        
    },
    {
        "id": 1,
        "name": "Home-Chef",
        "image": recipes,
        "description": "Recipe website that uses the meal DB API with a nice responsive user interface. It uses the mealdb api and googles firebase on the backend. This site provides auth and uses the firestore for data management.",
        "tech1": "Vuejs",
        "tech3": "Tailwindcss",
        "tech4": "Firebase",
        "website": "https://recipes-sigma-livid.vercel.app/",
        "github": "https://github.com/woodyrr/recipes"
        
    },
    {
        "id": 2,
        "name": "Soleilla",
        "image": Soleilla,
        "description": "An E-commerse application.",
        "tech1": "html",
        "tech2": "CSS",
        "tech3": "Tailwindcss",
        "tech4": "Javascript",
        "website": "https://woodyrr.github.io/Soleilla/",
        "github": "https://github.com/woodyrr/Soleilla/tree/main2"
        
    },
    {
        "id": 3,
        "name": "Threeb",
        "image": threeb,
        "description": "Anime/manga website where user can search for their favorite series to add and save their reading/watching status for next time. This site uses an anime api and taught me how to use use vuejs, Locale storage and apis.",
        "tech1": "Vuejs",
        "tech2": "CSS",
        "tech3": "Tailwindcss",
        "tech4": "Javascript",
        "website": "https://threeb.vercel.app/",
        "github": "https://github.com/woodyrr/TWB"
        
    },
    
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
