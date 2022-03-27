<template>
  <div class="header-main">
    <SiteLogo class="header-logo" />
    <div class="header-main-separator" />
    <div class="header-main-location">
      <div>
        <div class="txt-location"><IconMap class="icon-txt"/>Москва</div>
        <div class="txt-small-main">7 клиник <span>рядом с Вами!</span></div>
      </div>
    </div>
    <div class="header-main-contacts">
      <div class="txt-note">Запись на приём</div>
      <div class="txt-phone">
        <Phone class="icon" />
        <VectorGroup class="icon" />
        <VectorGroupWhatsupp class="icon" />
        <span>8 (495) 540-48-03</span>
      </div>
      <a class="txt-email" href="mailto:medgorod@bk.ru">medgorod@bk.ru</a>
    </div>
  </div>
</template>

<script>
import SiteLogo from '@/assets/Site-logo.svg?inline'
import IconMap from '@/assets/Icon-map.svg?inline'
import VectorGroup from '@/assets/Vector-group.svg?inline'
import Phone from '@/assets/Phone.svg?inline'
import VectorGroupWhatsupp from '@/assets/Vector-group-whatsupp.svg?inline'

export default {
  components: {
    SiteLogo,
    IconMap,
    VectorGroup,
    Phone,
    VectorGroupWhatsupp,
  }  
}
</script>

<style scoped>
.header-main {
  display: flex;
  padding-top: 12px;
  padding-bottom: 12px;
}

.header-main-location {
  display: flex;
  flex-grow: 1;
  align-items: center;
}

.header-main-location .txt-location {
  color:#035063;
  font-style: normal;
  font-weight: 800;
  font-size: 16px;
  line-height: 150%;
}

.header-main-location .txt-small-main {
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 143%;
  color: #014751;
}

.header-main-location .txt-small-main span{
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 143%;
  color: #808080;
}

.header-main-location .icon-txt {
  margin-right: 9px;
}

.header-main-location > * {
  align-self: center;
}

.header-main-contacts {
  text-align: right;
}

.header-main-contacts .txt-note{
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 143%;
  color: #035063;
  opacity: 0.6;
}

.header-main-contacts .txt-phone {
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 133%;
  color: #035063;
  
}

.header-main-contacts .txt-phone > span {
  font-size: inherit;
  white-space: nowrap;
}

.header-main-contacts .txt-email {
  font-style: normal;
  font-weight: 600;
  font-size: 14px;
  line-height: 143%;
  color: #014751;
  cursor: pointer;
  text-decoration: none;
}

.header-main-separator {
  border: 1px solid rgba(233 233 233 / 80%);
  margin: 16px 32px;
  width: 2px;
}

.header-main-contacts .icon {
  cursor: pointer;
  transition: 0.5s; 
  text-align: center; 
}

.header-main-contacts .icon:hover {
  transform: scale(1.2);
}

@media (max-width: 960px){
  .header-main-separator {
    display: none;
  }
}

@media (max-width: 960px){
  .header-main {
    flex-wrap: wrap;
  }

  .header-main .header-logo {
    width: 100%;
    margin-bottom: 16px;
  }
}
</style>
