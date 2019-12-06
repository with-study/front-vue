<template>
  <li>
    <p>{{ title }}</p>
    <p>{{ date }}</p>
  </li>
</template>

<script>
export default {
  name: 'NoticeItem',
  props: {
    title: String,
    date: String
  }
}
</script>

<style>

</style>
