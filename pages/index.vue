<template>
  <div class="w-screen h-screen flex items-center justify-center bg-gray-100">
    <div class="container mx-auto px-4">
      <div class="max-w-sm mx-auto relative">
        <div class="flip-card w-full h-64 sm:h-72 sm:w-96" :class="{ 'is-flipped': isFlipped }">
          <div class="flip-card-inner">
            <div class="flip-card-front bg-gradient-to-br from-blue-600 to-blue-400 text-white flex flex-col items-center justify-center p-6 rounded-lg">
              <h1 class="text-3xl sm:text-4xl font-bold text-center mb-2">Bhagyalaxmi Traders</h1>
              <p class="text-lg">All type of Printing</p>
            </div>
            <div class="flip-card-back bg-white text-gray-800 p-6 sm:p-8 rounded-lg">
              <h2 class="text-2xl font-semibold mb-4 text-blue-600">Bhavesh Shah</h2>
              <div class="space-y-3">
                
                <div class="flex items-center">
                  <svg class="w-5 h-5 mr-2 mt-1 text-blue-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path></svg>
                  <div class="w-full">
                    <p class="text-sm">+91 9824019610</p>
                    <p class="text-sm">+91 9429023960</p>
                  </div>
                </div>

                <div class="flex items-start ">
                  <svg class="w-5 h-5 mr-2 mt-1 text-blue-500 flex-shrink-0" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                  <div class="w-full">
                    <a href="mailto:bhavesh_bt@yahoo.co.in" class="text-sm text-blue-600 hover:underline block">bhavesh_bt@yahoo.co.in</a>
                    <a href="mailto:hetprints@gmail.com" class="text-sm text-blue-600 hover:underline block">hetprints@gmail.com</a>
                  </div>
                </div>
              
                <div class="mt-6 flex items-start">
                  <a href="https://maps.google.com/?q=B-122,123+B.G.+Tower,+Delhi+Darwaja,+Ahmedabad-380004" target="_blank" rel="noopener noreferrer" class="flex-shrink-0">
                    <svg class="w-5 h-5 mr-2 mt-1 text-blue-500" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
                  </a>
                  <div class="w-full">
                    <p class="text-sm">B-122,123 1st Floor, B.G. Tower, Delhi Darwaja, Ahmedabad-380004</p>
                  </div>
                </div>
              </div>

            </div>
          </div>
        </div>
        <button @click="toggleFlip" class="absolute -bottom-4 right-4 bg-white hover:bg-gray-100 text-blue-600 font-bold py-2 px-4 rounded-full text-sm shadow-md transition duration-300 ease-in-out transform hover:scale-105">
          <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24"><path fill="currentColor" d="M11.412 16.962q-1.881-.24-3.147-1.639Q7 13.925 7 12q0-2.083 1.458-3.542Q9.917 7 12 7q1.925 0 3.323 1.256q1.398 1.255 1.639 3.136l-1.081-.317q-.324-1.35-1.393-2.212Q13.418 8 12 8q-1.65 0-2.825 1.175T8 12q0 1.425.872 2.5t2.203 1.4zm1.2 4.007q-.153.031-.306.031H12q-1.868 0-3.51-.708t-2.857-1.924t-1.924-2.856T3 12.003t.709-3.51Q4.417 6.85 5.63 5.634t2.857-1.925T11.997 3t3.51.709t2.859 1.924t1.925 2.857T21 12v.296q0 .148-.03.296L20 12.3V12q0-3.35-2.325-5.675T12 4T6.325 6.325T4 12t2.325 5.675T12 20h.3zm7.144-.18l-4.794-4.814l-.923 2.794L12 12l6.77 2.039l-2.795.923l4.814 4.794z"/></svg>
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const isFlipped = ref(false)

const toggleFlip = () => {
  isFlipped.value = !isFlipped.value
}
</script>

<style scoped>
.flip-card {
  perspective: 1000px;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.6s;
  transform-style: preserve-3d;
}

.flip-card.is-flipped .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front, .flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.flip-card-back {
  transform: rotateY(180deg);
}
</style>