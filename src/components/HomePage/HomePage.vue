<template>
  <div class="page-container">
    <div class="left-board">
      <LogoEmployees />
    </div>

    <ContentEmployees />
  </div>
</template>

<script>
import LogoEmployees from "@/assets/LogoEmployees";
import ContentEmployees from "@/components/HomePage/ContentEmployees/ContentEmployees";
export default {
  name: 'HomePage',
  components: {ContentEmployees, LogoEmployees},
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.left-board {
  height: 100vh;
  width: 88px;
  padding-top: 48px;
  background: #FFFFFF;
  border-right: 1px solid #DBDADA;
  box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.1);
}

.page-container {
  display: flex;
}
</style>
