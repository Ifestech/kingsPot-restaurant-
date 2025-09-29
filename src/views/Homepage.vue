<template>
  <div class="Container">
    <div class="flex flex-col md:flex-row gap-6 md:gap-20 lg:gap-16 justify-between">
        <!-- Image first on mobile -->
      <div class="order-1 md:order-2">
          <img src="../image/heroimg.png" alt="Hero Image" class="w-100 h-auto rounded-full shadow-lg items-center" />
      </div>

        <!-- Text second on mobile -->
      <div class="flex flex-col gap-8 md:gap-8 lg:gap-10 items-center md:items-start text-center md:text-left order-2 md:order-1">
        <h1 class="font-bold text-4xl sm:font-stretch-expanded font-stretch-normal xs:w-sm sm:w-md max-w-lg sm:text-5xl text-white text-center sm:text-justify sm:leading-[60px] lg:leading-[50px] md:text-left">
            Flavorful,<br>Tasty and,<br>Energizing
        </h1>
        <p class="text-md text-justify sm:text-lg xs:w-sm sm:w-md max-w-md text-white md:px-0">
            At Kingspot, we believe eating well should be simple and satisfying. That’s why our fresh, nutritious meals are ready for pickup—delicious, affordable, and tailored to your lifestyle. Healthy living, made easy.
        </p>
        <router-link to="menu">
          <button class="inline-flex items-center justify-center px-12 py-6 text-sm font-medium rounded-lg cursor-pointer text-white bg-orange-500 shadow-md transition-colors duration-200 ease-in-out 
            hover:bg-orange-600 active:bg-orange-700 active:shadow-inner">Order Now
          </button>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>

</style>