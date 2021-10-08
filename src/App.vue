<template>
  <div id="app" class="small-container">
    <h1>Employees</h1>


    <employee-form  @add:employee="addEmployee" /><br>
    <employee-table :employees="employees" />

  </div>
</template>

<script>
import EmployeeTable from "@/components/EmployeeTable";
import EmployeeForm from "@/components/EmployeeForm";

export default {
  name: "App",
  components: {
    EmployeeTable,
    EmployeeForm,
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: "Mahdon",
          surname: "Thaipuvnart",
          tel: "0840364668",
          email: "gundam7784@hotmail.com",
        },
        {
          id: 2,
          name: "Mahdon",
          surname: "Thaipuvnart",
          tel: "0840364668",
          email: "gundam7784@hotmail.com",
        },
        {
          id: 3,
          name: "Mahdon",
          surname: "Thaipuvnart",
          tel: "0840364668",
          email: "gundam7784@hotmail.com",
        },
      ]
    }
  },
  methods: {
    addEmployee(employee) {
      this.employees = [...this.employees, employee]
      console.log(this.employees)
    },
  },
};
</script>

<style>
.small-container {
  max-width: 1200px;
}
</style>
