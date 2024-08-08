<template>
    <div>
      <h1>Liste des employés</h1>
      <ol>
        <li v-for="employee in employees" :key="employee.id" @mouseover="hoveredEmployee = employee.id" @mouseout="hoveredEmployee = null" :class="{ hover: hoveredEmployee === employee.id }">
          {{ employee.name }}
        </li>
      </ol>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        employees: [
          { id: 1, name: 'Mamoudou Ba' },
          { id: 2, name: 'Bamba Fall' },
          { id: 3, name: 'Cheick diallo' },
          { id: 4, name: 'Coumba Sow' },
          { id: 5, name: 'Babs og' },
          { id: 6, name: 'Mamita Lam' }
        ],
        hoveredEmployee: null
      };
    }
  };
  </script>
  
  <style scoped>
  h1 {
    text-align: center;
    color: #333;
  }
  
  ol {
    padding: 0;
    list-style-type: decimal;
    margin: 0 auto;
    max-width: 400px;
  }
  
  li {
    padding: 10px;
    margin: 5px 0;
    background-color: #f9f9f9;
    border: 1px solid #ddd;
    border-radius: 5px;
    transition: background-color 0.3s, color 0.3s;
  }
  
  li.hover {
    background-color: #e0e0e0;
    color: #000;
  }
  </style>
  