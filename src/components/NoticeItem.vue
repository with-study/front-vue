<template>
  <li>
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

</style>
