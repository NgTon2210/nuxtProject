<template>
<div>
  <ul>
      <li>
          <nuxt-link to="/setting">this is setting index</nuxt-link>
      </li>
      <li>
          <nuxt-link to="/setting/tab1">tab1</nuxt-link>
      </li>
      <li>
          <nuxt-link to="/setting/tab2">tab2</nuxt-link>
      </li>
       <li>
          <nuxt-link to="/setting/tab3">tab3</nuxt-link>
      </li>
  </ul>
    <nuxt-child />
  </div>
</template>