<template>
  <div>
    <h3>Posts</h3>
    <ul class="list-group">
      <li class="list-group-item" v-for="p in getAllPosts" v-bind:key="p.id">
        {{ p.title }}
      </li>
    </ul>
  </div>
</template>

<script>
import { mapGetters } from "vuex";
export default {
  name: "Posts",
  computed: mapGetters(["getAllPosts"]),
};
</script>

<style scoped>
.list-group-item {
  color: brown;
}
</style>
