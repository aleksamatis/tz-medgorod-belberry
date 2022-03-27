<template>
<div>
  <ArrowBreadCrumb />
  <ul class="breadcrumb">
    <li><a href="#">Главная</a></li>
    <li><a href="#">Акции</a></li>
  </ul>
</div>
</template>
<style scoped>
ul.breadcrumb {
  padding: 10px 16px;
  list-style: none;
  background-color: transparent;
  display: inline;
}

ul.breadcrumb li {
  display: inline;
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  position: relative;
}

ul.breadcrumb li+li {
  padding-left: 12px;
}

ul.breadcrumb li+li::before {
  background: rgba(3 80 99 / 70%);
  width: 4px;
  height: 4px;
  border-radius: 100%;
  content: " ";
  position: absolute;
  left: 4px;
  top: 50%;
  transform: translateY(-50%);
}

ul.breadcrumb li a {
  color: rgba(3 80 99 / 70%);
  text-decoration: none;
}

ul.breadcrumb li a:hover {
  color: #11839E;
  text-decoration: none;
}
</style>
