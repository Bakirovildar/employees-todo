<template>
  <div>
    <HeaderContent/>
    <EmployeesList :employees="employees"/>
  </div>
</template>

<script>
import HeaderContent from "@/components/HomePage/ContentEmployees/content/header/HeaderContent";
import EmployeesList from "@/components/HomePage/ContentEmployees/content/EmployeesList/EmployeesList";

export default {
  components: {EmployeesList, HeaderContent},
  props: ['employees']
}
</script>

<style scoped>

</style>
