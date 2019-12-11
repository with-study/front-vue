<template>
  <li>
    <figure>
      <img src="" alt="">
    </figure>
    <p>{{ title }}</p>
    <p>{{ date }}</p>
    <p>{{ id }}</p>
    <p>
      {{ name }} |
      <span v-for="tag in tags">
        {{tag.key}}:{{tag.name}}
      </span>
    </p>
    <p><img v-bind:src="image" alt=""></p>
    <p>{{ price }}원</p>
    <p>{{ stock }}</p>
  </li>
</template>

<script>
export default {
  name: 'NoticeItem',
  props: {
    id: String,
    name: String,
    image: String,
    price: String,
    stock: String,
    tags: Array
  }
}
</script>

<style>
  ul {display: flex}
  li {list-style: none; padding-left:10px; border-right: 1px solid #ccc }
</style>
