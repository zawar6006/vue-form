<template>
  <table class="table" style="font-size: 9pt">
    <thead>
      <tr>
        <th>Date</th>
        <th>Subject</th>
        <th>To</th>
        <th>Name</th>
        <th>Student ID</th>
        <th>Major</th>
        <th>Faculty</th>
        <th>Telephone</th>
        <th>Email</th>
        <th>Reason</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(data, i) in formDataArray" v-bind:key="i">
        <td>{{ data.date }}</td>
        <td>{{ data.subject }}</td>
        <td>{{ data.to }}</td>
        <td>{{ data.name }}</td>
        <td>{{ data.studentID }}</td>
        <td>{{ data.major }}</td>
        <td>{{ data.faculty }}</td>
        <td>{{ data.telephone }}</td>
        <td>{{ data.email }}</td>
        <td>{{ data.reason }}</td>
      </tr>
    </tbody>
  </table>
</template>
<script setup>
defineProps({
  formDataArray: Array,
});
</script>
<style scoped></style>
