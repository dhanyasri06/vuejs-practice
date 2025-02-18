<script>
export default {
  data() {
    return {
      count: 0,
      name: "shiva",
      status: "inactive",
      tasks: ["Task One", "Task Two", "Task Three", "Task Four"],
      link: "https://",
    };
  },
  methods: {
    toggleStatus() {
      if (this.status == "inactive") {
        this.status = "active";
      } else if (this.status == "active") {
        this.status = "pending";
      } else if (this.status == "pending") {
        this.status = "inactive";
      }
    },
  },
};
</script>
<template>
  <p>{{ count }}</p>
  <p>User is : {{ status.charAt(0).toUpperCase() + status.slice(1) }}</p>
  <input type="text" name="" id="" />

  <h3>Tasks :</h3>
  <ul>
    <li v-for="task in tasks">{{ task }}</li>
  </ul>
  <a :href="link">Click for google </a>
  <button v-on:click="toggleStatus">Change Status</button>
</template>
