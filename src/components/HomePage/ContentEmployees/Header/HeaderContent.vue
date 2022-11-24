<template>
  <div class="header-container">
    <span class="header-name">Сотрудники</span>
    <div class="company-name">
      <div class="circle">O</div>
      <span>ООО «Модуль»</span>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.header-container {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin: 0 100px;
}

.header-name {
  font-family: 'PF DinDisplay Pro';
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 30px;
  display: flex;
  align-items: center;
  color: #353535;
}

.company-name {
  display: flex;
  align-items: center;
  margin-right: 150px;
}

.circle {
  width: 24px;
  height: 24px;
  margin-right: 8px;
  background: #E31243;
  border-radius: 50%;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 900;
  font-size: 16px;
  line-height: 22px;
}
</style>
