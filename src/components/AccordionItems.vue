<template>
  <div id="accordion" v-for="(data, i) in formDataArray" v-bind:key="i">
    <div class="card">
      <div class="card-header" :id="'heading' + i">
        <h5 class="mb-0">
          <button
            class="btn btn-link collapsed"
            data-toggle="collapse"
            :data-target="'#collapse' + i"
            aria-expanded="true"
            :aria-controls="'collapse' + i"
          >
            [ {{ data.date }} ] {{ data.name }}
          </button>
        </h5>
      </div>

      <div
        :id="'collapse' + i"
        class="collapse show"
        aria-labelledby="headingOne"
        data-parent="#accordion"
      >
        <div class="card-body">
          <p class="mb-0"><strong>วันที่: </strong>{{ data.date }}</p>
          <p class="mb-0"><strong>เรื่อง: </strong>{{ data.subject }}</p>
          <p class="mb-0"><strong>เรียน: </strong>{{ data.to }}</p>
          <p class="mb-0"><strong>ชื่อ: </strong>{{ data.name }}</p>
          <p class="mb-0">
            <strong>รหัสนักศึกษา: </strong>{{ data.studentID }}
          </p>
          <p class="mb-0"><strong>สาขาวิชา: </strong>{{ data.major }}</p>
          <p class="mb-0"><strong>คณะ: </strong>{{ data.faculty }}</p>
          <p class="mb-0"><strong>โทรศัพท์: </strong>{{ data.telephone }}</p>
          <p class="mb-0"><strong>Email: </strong>{{ data.email }}</p>
          <p class="mb-0"><strong>เหตุผลประกอบ: </strong>{{ data.reason }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup>
defineProps({
  formDataArray: Array,
});
</script>
<style scoped></style>
