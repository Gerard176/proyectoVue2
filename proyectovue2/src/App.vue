<script setup>

  import { ref, computed} from 'vue'
  const users = [
    {
      name: 'pepito',
      lastname: 'perez',
      
    },
    {
      name: 'juliana',
      lastname: 'perez',
      age: '10000'
    }

  ]
  const num = ref(2)
  const computado =  computed(function(){
    return num.value > 0 ? num.value*3 : 0
  })
</script>

<template>
  Valor computado: {{ computado }}
  <div v-for="(user,index) in users" :key="index"> 
  Nombre completo: {{ user.name }} {{ user.lastname }}
  <span v-if="user.age">
    Edad: {{ user.age }}
  </span>
  </div>
</template>

<style scoped>


</style>
