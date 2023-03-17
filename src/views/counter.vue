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
    <div class = "container">
        <h1 id = "counterTxt">Counter</h1>

        
                <h1 id= "count" > {{ count }}</h1>
           

           
                    <input id = "userInput" type="text" placeholder=" Enter value here" v-model="num" />
              



                    <div class="buttonContainer">
                    <button id = "addBtn" @click="setValue(num)">Add</button>
                        <button id = "decreaseBtn" @click="decrement">Decrement</button>
                        <button id = "resetBtn" @click="reset" >Reset</button>
                        <button id = "increaseBtn" @click="increment" >Increment</button>
        
                    </div>
         

          </div>  
          
            <router-link to='/'>
              <button id = "returnBtn">Home page</button>
            </router-link>

            
       
    
</template>

