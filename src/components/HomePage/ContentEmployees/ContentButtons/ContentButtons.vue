<template>
  <div class="buttons-container">
    <div class="add-new-department">
      <ButtonComponent :type='1'/>
      <ButtonComponent :type='2'/>
    </div>

    <div class="add-new-department">
      <ButtonComponent :type="3" />
    </div>
  </div>
</template>

<script>
import ButtonComponent from "@/components/general/ButtonComponent";

export default {
  components: {ButtonComponent}
}
</script>

<style scoped>
.buttons-container {
  margin-top: 30px;
  margin-left: 100px;
  display: flex;
  justify-content: space-between;
  width: 100%;
}

.add-new-department {
  display: flex;
}
</style>
