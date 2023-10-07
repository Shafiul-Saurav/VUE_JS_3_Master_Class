<template>
  <input type="text" v-model="course.name" />
  <h1>{{ staticCourse }}</h1>
  <h1>{{ course.name }}</h1>
  <h2>Mentor: {{ course.mentor }}</h2>
  <h2>Platform: {{ course.platform }}</h2>
  <p>Student: {{ course.student }}</p>
  <br />
  <input type="number" v-model="count" />
  <div>
    <button @click="count++">+</button>
    <h3>{{ count }}</h3>
    <button @click="count--">-</button>
  </div>
</template>

<script setup>
import { ref, reactive } from "vue";
let count = ref(0);
const staticCourse = "Laravel & Vue Master Class";
count.value = 10;
let course = reactive({
  name: "Vue Js 3 Master Class With Fundamental",
  mentor: "Mohammad Ibrahim",
  student: "Shafiul Saurav",
  platform: "Instructory",
});
</script>
