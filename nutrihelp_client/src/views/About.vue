<template>
  <div>
    <h1 class="text-4xl font-bold mb-4">About Personalized Nutrition Advisor</h1>
    <p class="text-lg mb-6">
      Personalized Nutrition Advisor is a project aimed at helping individuals achieve their health and wellness goals through customized dietary recommendations. By analyzing personal health data and preferences, we offer tailored advice and meal plans to support your journey towards a healthier lifestyle.
    </p>
    <h2 class="text-2xl font-semibold mb-4">Enter Your Personal Information</h2>
    <form @submit.prevent="handleSubmit" class="space-y-4">
      <div>
        <label for="name" class="block text-lg font-medium text-gray-700">Name</label>
        <input
          type="text"
          id="name"
          v-model="formData.name"
          class="mt-1 p-2 block w-full border border-gray-300 rounded-md"
          required
        />
      </div>
      <div>
        <label for="email" class="block text-lg font-medium text-gray-700">Email</label>
        <input
          type="email"
          id="email"
          v-model="formData.email"
          class="mt-1 p-2 block w-full border border-gray-300 rounded-md"
          required
        />
      </div>
      <div>
        <label for="age" class="block text-lg font-medium text-gray-700">Age</label>
        <input
          type="number"
          id="age"
          v-model="formData.age"
          class="mt-1 p-2 block w-full border border-gray-300 rounded-md"
          required
        />
      </div>
      <div>
        <label for="height" class="block text-lg font-medium text-gray-700">Height (cm)</label>
        <input
          type="number"
          id="height"
          v-model="formData.height"
          class="mt-1 p-2 block w-full border border-gray-300 rounded-md"
          required
        />
      </div>
      <div>
        <label for="weight" class="block text-lg font-medium text-gray-700">Weight (kg)</label>
        <input
          type="number"
          id="weight"
          v-model="formData.weight"
          class="mt-1 p-2 block w-full border border-gray-300 rounded-md"
          required
        />
      </div>
      <button
        type="submit"
        class="w-full py-2 px-4 bg-blue-600 text-white font-semibold rounded-md hover:bg-blue-700"
      >
        Submit
      </button>
    </form>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'About',
  setup() {
    const formData = ref({
      name: '',
      email: '',
      age: '',
      height: '',
      weight: ''
    });

    const handleSubmit = () => {
      console.log('Form Data:', formData.value);
      // Here you can add logic to send the form data to your backend or API.
    };

    return {
      formData,
      handleSubmit
    };
  }
};
</script>

<style scoped>
</style>
