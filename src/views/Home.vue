
<script setup>

import { RouterLink } from "vue-router";


</script>

<template>
  <section class = "homeSection">
   
            <h5 >
              Welcome to my Vue counter App
            </h5>

            <RouterLink to="/counter" >
              <button class="startButton">click to start</button>
            </RouterLink>
         
  </section>
</template>


