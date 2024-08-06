<template>
    <HelloWord />
         
        <!-- <template v-slot:name>
              {{ user.name }}    
        </template>

        <template v-slot:age>
            {{ user.age}}
        </template> -->
        <div :class="{ 'text-green':user.age>23}"> {{ user.name }}</div>
    
    <!-- <HelloWord :user="user" /> -->
    
    <!-- <h2>{{ subTitle }}</h2> -->
    <!-- <input type="text" v-model="user.name" placeholder="Enter name">
    <input type="number" v-model="user.age" placeholder="Enter age"> -->

  </template>
  
  <script setup>
  
  import HelloWord from './components/HelloWord.vue';
  import { reactive } from 'vue';
  
  const user = reactive({
    name: 'NordCoders',
    age: 30,
  });
  
  const display = () =>{
    console.log(user.name,user.age);
  }
  </script>
  
  <style scoped>
    .text-red {
        
        color: indianred;
    }
    .text-green {
        color: green;
    }
  </style>
  