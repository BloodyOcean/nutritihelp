<template>
    <li 

      class="text-md no-underline text-white hover:text-blue-dark ml-2 px-1 text-nowrap self-center"
      :class="{ 'bg-gray-700': isActive }" 
      @click="$emit('click')"
    >
      {{ label }}
    </li>
  </template>
  
  <script>
  export default {
    name: 'NavItem',
    props: {
      label: {
        type: String,
        required: true
      },
      route: {
        type: String,
        required: true
      },
      isActive: {
        type: Boolean,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  /* Additional styles if needed */
  </style>
  