<template>
  <a class="link">
    <slot/>
  </a>
</template>

<style scoped>
.link {
  display: block;
  text-decoration: none;
  color: #035063;
  cursor: pointer;
  font-family: 'Proxima Nova Th', var(--bs-body-font-family);
  font-weight: 800;
}

.link:hover, .link:active, .link:focus {
  color: #11839E;
}

.link >>> svg {
  vertical-align: text-bottom;
}

.link:hover  >>> svg *, .link:active  >>> svg *, .link:focus >>> svg * {
  stroke: #11839E;
}
</style>
