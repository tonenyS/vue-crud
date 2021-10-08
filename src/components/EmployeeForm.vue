<template>
  <div id="employee-form">
    <form @submit.prevent="handleSubmit">
      <label> Name:</label>
      <input v-model="employee.name" type="text" />
      <label> Surname:</label>
      <input v-model="employee.surname" type="text" />
      <label> Tel:</label>
      <input v-model="employee.tel" type="text" />
      <label> Email:</label>
      <input v-model="employee.email" type="text" />
      <button>Add Employee</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "employee-form",
  data() {
    return {
      employee: {
        name: "",
        surname: "",
        tel: "",
        email: "",
      },
    };
  },
  methods: {
    handleSubmit() {
      this.$emit('add:employee', this.employee);
    },
  },
};
</script>

