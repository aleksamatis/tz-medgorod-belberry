<template>
<div>
  <Header />
  <div class="section-action">
    <SectionAction class="main-content" />
    <Image31 class="section-action-image" />
  </div>
  <Banners class="main-content" />
</div>
</template>

<script>
import Image31 from '@/assets/Image-31.svg?inline'
export default {
  name: 'IndexPage',
  components: {
    Image31,
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: 'Proxima Nova Rg', 'Proxima Nova Th', var(--bs-body-font-family);
}

*, *::before, *::after {
  box-sizing: border-box;
}

.section-action {
  background: rgba(239 239 239 / 30%);
  position: relative;
}

.section-action-image {
  position: absolute;
  left: 60%;
  top: 10px;
}

.main-content {
  max-width: 1312px;
  margin: 0 auto;
}

@media (max-width: 1360px){
  .main-content {
    padding-left: 20px;
    padding-right: 20px;
  }
}

@media (max-width: 960px) {
  .section-action-image {
    display: none;
  }
}
</style>
