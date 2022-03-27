<template>
  <div class="arrow-bread-crumb">
    <VectorLeftArrow />
  </div>
</template>

<script>
import VectorLeftArrow from '@/assets/Vector-left-arrow.svg?inline'
export default {
  components: {
    VectorLeftArrow,
  }  
}
</script>

<style scoped>
.arrow-bread-crumb {
  background-color: rgba(1 71 81 / 8%);
  border-radius: 8px;
  cursor: pointer;
  display: inline-flex;
  height: 35px;
  width: 35px;
  justify-content: center;
  align-items: center;
}
</style>
