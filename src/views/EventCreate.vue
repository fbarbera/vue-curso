<template>
  <div>
    <h1>Create an Event, {{ userName }}</h1>
    <p>This event was created by {{ userId }}</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: mapState({
    userName: state => state.user.name,
    userId: state => state.user.id,
    categories: state => state.categories
  })
}
</script>

<style lang="scss" scoped></style>
