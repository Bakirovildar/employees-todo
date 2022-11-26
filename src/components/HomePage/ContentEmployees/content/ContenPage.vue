<template>
  <div>
    <HeaderContent/>
    <EmployeesList :employees="employees" @deleteEmploy="deleteEmploy"/>
  </div>
</template>

<script>
import HeaderContent from "@/components/HomePage/ContentEmployees/content/header/HeaderContent";
import EmployeesList from "@/components/HomePage/ContentEmployees/content/EmployeesList/EmployeesList";

export default {
  components: {EmployeesList, HeaderContent},
  props: ['employees'],
  emits: ['deleteEmploy'],
  methods: {
    deleteEmploy(id) {
      this.$emit('deleteEmploy', id)
    }
  }
}
</script>

<style scoped>

</style>
