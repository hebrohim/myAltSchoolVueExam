<script setup>
import useCounter from '../composable/useCount.js'
import { useStore } from 'vuex'
import { computed } from 'vue'
import { useState } from 'vuex-composition-helpers/dist'


const store = useStore()
const { count } = useState(['count'])


let num = ''
const { increment, decrement, reset, setValue } = useCounter(num, store)
</script>

<template>
    <div>
        <h1>Counter</h1>

        
                <h1 > {{ count }}</h1>
           

           
                    <input type="text" class="h-10 text-black px-2  outline-none in rounded-md  text-2xl" placeholder=" value" v-model="num" />
                    <button class=" text-2xl to px-3 p-auto rounded-md " @click="setValue(num)">Add</button>
              



                    <div class="centered mt-6 gap-5">
                        <button @click="decrement">Decrement</button>
                        <button @click="reset" >Reset</button>
                        <button @click="increment" >Increment</button>
                    </div>
                </div>
         

      
            <router-link to='/'>
                Return Home
            </router-link>
       
    
</template>

