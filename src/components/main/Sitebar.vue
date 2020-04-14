<template>
  <ul class="sidenav app-sidenav" :class="{'open': value}">

      <router-link
        v-for="link of links"
        :key="link.url"
        tag="li"
        active-class="active"
        :to="link.url"
        :exact="link.exact"
      >
          <a :href="link.url" class="waves-effect waves-orange pointer">{{link.name}}</a>
      </router-link>

  </ul>
</template>
<script>
export default {
    data: ()=>({
      links:[
        {name:"Счет", url: "/", exact: true},
        {name:"История", url: "/history"},
        {name:"Планирование", url: "/planning"},
        {name:"Новая запись", url: "/record"},
        {name:"Категории", url: "/category"}
      ]
    }),
    props:['value']
}
</script>
