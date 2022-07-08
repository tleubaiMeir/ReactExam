<template>
  <div class="container">
    <h2 class="text-center">Тестовое задание на Vue.js</h2>
    <p class="human-content" v-for="human in humans" :key="human.id" :class="{ 'human-content_active': human.isActive }"
      @click="human.isActive = !human.isActive">
      My name is {{ human.name }} and surname {{ human.surname }} I work at company called ‘{{ human.company }}'
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      humans: [
        {
          name: 'John',
          surname: 'Smith',
          age: 20,
          company: 'Google',
          id: 1,
          isActive: false
        },
        {
          name: 'Thomas',
          surname: 'Anderson',
          age: 24,
          company: 'Metacortex',
          id: 2,
          isActive: false
        },
        {
          name: 'Steve',
          surname: 'Jobs',
          age: 40,
          company: 'Apple',
          id: 3,
          isActive: false
        },
        {
          name: 'Mark',
          surname: 'Zucerberg',
          age: 33,
          company: 'FaceBook',
          id: 4,
          isActive: false
        }
      ]
    }
  },

}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}

.container {
  max-width: 1280px;
  margin: 0 auto;
}

.text-center {
  text-align: center;
}

.human-content {
  padding: 15px 20px;
  border: 1px solid black;
  border-radius: 6px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.5);
  margin-top: 20px;
}

.human-content_active {
  background-color: darkred;
  color: white;
}
</style>