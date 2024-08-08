<template>
  <div id="app">
    <employee-list></employee-list>
  </div>
</template>

<script>
import EmployeeList from './components/EmployeeList.vue';

export default {
  components: {
    EmployeeList
  }
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  padding: 20px;
  background-color: #f5f5f5;
  margin: 0;
}

#app {
  text-align: center;
}
</style>
