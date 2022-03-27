<template>
  <div class="header-nav">
    <div class="header-nav-items">
      <HeaderNavLink><VectorHome class="header-nav-home" /></HeaderNavLink>
      <HeaderNavLink><VectorMenu class="header-nav-menu"/>Услуги</HeaderNavLink>
      <HeaderNavLink>О клинике</HeaderNavLink>
      <HeaderNavLink>Врачи</HeaderNavLink>
      <HeaderNavLink>Цены</HeaderNavLink>
      <HeaderNavLink>Отзывы</HeaderNavLink>
      <HeaderNavLink>Акции</HeaderNavLink>
      <HeaderNavLink>Клиники</HeaderNavLink>
    </div>
    <div class="header-nav-controls">
      <VectorSearch class="header-nav-search"/>
      <el-button type="primary" round>Обратный звонок</el-button>
    </div>
  </div>
</template>

<script>
import VectorSearch from '@/assets/Vector-search.svg?inline'
import VectorHome from '@/assets/Vector-home.svg?inline'
import VectorMenu from '@/assets/Vector-menu.svg?inline'

export default {
  components: {
    VectorSearch,
    VectorHome,
    VectorMenu,
  }  
}
</script>

<style scoped>
  .header-nav {
    display: flex;
    align-items: center;
    padding-top: 16px;
    padding-bottom: 16px;
  }

  .header-nav > div {
    font-style: normal;
    font-weight: 800;
    font-size: 16px;
    line-height: 150%;
    text-transform: uppercase;
  }

  .header-nav-home {
    flex-grow: 0;
    flex-shrink: 0;
    width: 28px;
    cursor: pointer;
  }

  .header-nav-items {
    display: flex;
    flex-grow: 1;
    flex-shrink: 1;
    align-items: center;
  }

  .header-nav-items > * {
    padding: 0 32px;
    border-right: 1px solid rgba(233 233 233 / 80%);
    white-space: nowrap;
  }

  .header-nav-items > *:first-child {
    padding-left: 0;
  }

  .header-nav-items > *:last-child {
    border-right: 0;
  }

  .header-nav >>> .el-button.el-button--primary {
    line-height: 150%;
    background: #FF7512;
    border: 1px solid #FF7512;
    padding: 10px 32px;
    font-size: 16px;
    border-radius: 38px;
    font-weight: 700;
  }

  .header-nav >>> .el-button.el-button--primary:active, .header-nav >>> .el-button.el-button--primary:hover {
    background: #F78F45;
    border: 1px solid #F78F45;
    box-shadow: 0 4px 16px rgba(255 140 105 / 29%);
  }

  .header-nav-menu {
    margin-right: 16px;
  }

  .header-nav-search {
    margin-right: 40px;
    cursor: pointer;
  }

  .header-nav-home, .header-nav-search {
    opacity: 0.16;
  }

@media (max-width: 1360px){
  .header-nav-items > * {
    padding: 0 12px;
  }
}

@media (max-width: 1360px){
  .header-nav-search {
    margin-right: 12px;
  }
}

@media (max-width: 1360px){
   .header-nav > div {
    font-style: normal;
    font-weight: 800;
    font-size: 12px;
    line-height: 150%;
    text-transform: uppercase;
  }
}

.header-nav-controls {
  display: flex;
  align-items: center;
}

@media (max-width: 1360px){
  .header-nav >>> .el-button.el-button--primary {
    line-height: 150%;
    background: #FF7512;
    border: 1px solid #FF7512;
    padding: 6px 12px;
    font-size: 12px;
    border-radius: 38px;
    font-weight: 700;
  }
}

@media (max-width: 960px) {
  .header-nav {
    flex-wrap: wrap;
  }

  .header-nav-items {
    flex-wrap: wrap;
    gap: 10px;
  }

  .header-nav-controls {
    margin-top: 16px;
  }
}

</style>
