<template>
  <div>
    <HeaderContent @clickAllChecked="clickAllChecked"/>
    <EmployeesList
        :employees="employees"
        @deleteEmploy="deleteEmploy"
    />
  </div>
</template>

<script>
import HeaderContent from "@/components/HomePage/ContentEmployees/content/header/HeaderContent";
import EmployeesList from "@/components/HomePage/ContentEmployees/content/EmployeesList/EmployeesList";

export default {
  components: {EmployeesList, HeaderContent},
  props: ['employees'],
  emits: ['deleteEmploy', 'clickAllChecked'],
  methods: {
    deleteEmploy(id) {
      this.$emit('deleteEmploy', id)
    },
    clickAllChecked(check) {
      this.$emit('clickAllChecked', check)
    }
  }
}
</script>

<style scoped>

</style>
