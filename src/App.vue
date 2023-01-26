<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Footer from './components/Footer.vue'
</script>

<template>
<header class="fixed top-0 left-0 right-0 z-40">
     <nav class="main-nav">
        <div class="container xl:max-w-6xl mx-auto px-4">
          <div class="lg:flex lg:justify-between">
          	<div class="flex justify-between">
	            <div class="mx-w-10 text-4xl font-bold capitalize text-gray-900 flex items-center">Jetmoney</div>
		          
	          </div>
            
            <div class="flex flex-row">
              <!-- nav menu -->
              <ul class="navbar bg-white lg:bg-transparent w-full hidden text-center lg:text-left lg:flex lg:flex-row text-gray-900 text-sm items-center font-bold">
                <li class="relative hover:text-black">
                  <RouterLink to="/" class="active block py-3 lg:py-7 px-6 border-b-2 border-transparent" >Главное</RouterLink>
                </li>
                <li class="relative hover:text-black">
                  <RouterLink to="/aboutus" class="block py-3 lg:py-7 px-6 border-b-2 border-transparent">О нас</RouterLink>
                </li>
                <li class="relative hover:text-black">
                   <RouterLink to="/work" class="block py-3 lg:py-7 px-6 border-b-2 border-transparent">Принцип работы</RouterLink>
                </li>
                <li class="relative hover:text-black">
                   <RouterLink to="quest" class="block py-3 lg:py-7 px-6 border-b-2 border-transparent" >Вопросы</RouterLink>
                </li>
                <li class="relative hover:text-black">
                  <a class="block py-3 lg:py-7 px-6 border-b-2 border-transparent" href="https://t.me/jetmoneyy" >Телеграм</a>
                </li>
               
              </ul>
            </div>
          </div>
        </div>
     </nav>
  </header>
  <RouterView />
  <Footer/>
</template>



