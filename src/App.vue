<template>
  <form @submit.prevent="submitForm" class="form">
    <label for="inputName">Name:</label>
    <input type="text" id="inputName" v-model="formData.name" class="input">
    
    <label for="inputEmail">Email:</label>
    <input type="email" id="inputEmail" v-model="formData.email" class="input">

    <div class="Skills">
      Skills:
      <label><input type="checkbox" v-model="skills" value="react.js">React.js</label>
      <label><input type="checkbox" v-model="skills" value="vue.js">Vue.js</label>
      <label><input type="checkbox" v-model="skills" value="node.js">Node.js</label>
    </div>

    <button type="submit" class="button">Submit</button>
  </form>
</template>

<script setup>
import { ref } from 'vue';


const formData = ref({
  name: '',
  email: ''
});


const skills = ref([]);


const submitForm = () => {
  
  console.log('Form data:', formData.value);
  
  console.log('Skills:', skills.value);

};
</script>

<style scoped>
.form {
  width: 300px;
  margin: auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.input {
  width: 100%;
  margin-bottom: 10px;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

.Skills{
  margin-bottom: 10px;
}

.Skills label {
  display: block;
  margin-bottom: 5px;
}

.button {
  width: 100%;
  padding: 10px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

.button:hover {
  background-color: #0056b3;
}
</style>
