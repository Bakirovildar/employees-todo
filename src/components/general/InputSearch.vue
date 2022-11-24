<template>
  <div class="message-send-input">
    <input
        v-model="searchValue"
        type="text"
        placeholder="Поиск по ФИО"
        style="color: #8C9EB4;"
    >
    <div class="message-send-input-add__file"><LogoSearch/></div>
  </div>
</template>

<script>
import LogoSearch from "@/assets/LogoSearch";
export default {
  components: {LogoSearch},
  data() {
    return {
      searchValue: ''
    }
  }
}
</script>

<style scoped>

.message-send-input {
  margin-top: 30px;
  margin-left: 100px;
  background: #FFFFFF;
  border: 1px solid #DBDADA;
  box-shadow: inset 0px 1px 4px rgba(0, 0, 0, 0.2);
  border-radius: 1px;
  display: flex;
  justify-content: space-between;
  height: 40px;
  width: 304px;
  align-items: center;
}

input {
  height: 36px;
  width: 100%;
  border: none;
  outline: none;
  padding: 0 12px;
}

.message-send-input-add__file {
  width: 28px;
  height: 28px;
  background: #FFFFFF;
  border-radius: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 10px 0 4px;
}
</style>
