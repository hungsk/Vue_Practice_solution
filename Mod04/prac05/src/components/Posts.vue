<template>
  <div>
    <h3>Posts</h3>
    <ul class="list-group">
      <li class="list-group-item" v-for="p in getAllPosts" v-bind:key="p.id">
        <strong> User Id : </strong> {{ p.userId }} <br />
        <strong> Title : </strong> {{ p.title }} <br />
        <strong> Body : </strong> {{ p.body }} <br />

      </li>
    </ul>
  </div>
</template>

<script>
import { mapGetters, mapActions } from "vuex";
export default {
  name: "Posts",
  computed: {
    ...mapGetters(["getAllPosts"])
  },
  methods: {
    ...mapActions(["getPostsAction"]) 
  },
  created() {
    this.getPostsAction();
  },
};
</script>

<style scoped>
.list-group-item {
  color: brown;
}
</style>
