<template>
  <div class="contentEmployees">
    <HeaderContent/>
    <ContentButtons />
    <InputSearch/>
    <ContenPage/>
  </div>
</template>

<script>
import HeaderContent from "@/components/HomePage/ContentEmployees/Header/HeaderContent";
import ContentButtons from "@/components/HomePage/ContentEmployees/ContentButtons/ContentButtons";
import InputSearch from "@/components/general/InputSearch";
import ContenPage from "@/components/HomePage/ContentEmployees/content/ContenPage";

export default {
  components: {ContenPage, InputSearch, ContentButtons, HeaderContent}
}
</script>

<style scoped>
.contentEmployees {
  margin: 47px 100px;
  width: 100%;
}
</style>
