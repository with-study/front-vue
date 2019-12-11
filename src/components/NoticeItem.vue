<template>
  <li>
    <p>{{ name }}</p>
    <p>가격 : {{ price }}</p>
    <p>재고 : {{ stock }}</p>
    <img :src="src" alt="name" />
    <p v-for="tag in tags"><span>{{ tag.key }}</span> : <span>{{ tag.name }}</span></p>
  </li>
</template>

<script>
export default {
  name: 'NoticeItem',
  props: {
    name: String,
    price: String,
    stock: String,
    src: String,
    tags: {
      key: String,
      name: String
    }
  }
}
</script>

<style>
  ul {display: flex}
  li {list-style: none; padding-left:10px; border-right: 1px solid #ccc }
</style>
