<template>
  <div>
    <h3>Posts</h3>

    <ul class="list-group">
      <li v-for="p in getAllPosts" :key="p.id">
        <strong>User ID: {{p.userId}}</strong>
        <strong>Title: {{p.title}}</strong>
        <strong>Body : {{p.body}}</strong>
        <div class="mt-3">
          <div class="btn-groud" role="groud" aris-label="Basic exmple">
            <button type="button" class="btn btn-danger"  @click="removePostAction(p.id)">Delete</button>
          </div>
          <router-link class="btn btn-success" :to="`/edit/${p.id}`">Edit</router-link>
        </div>
      </li>
      <!-- <li class="list-group-item" v-for="p in getAllPosts" v-bind:key="p.id">
        {{ p.title }}
      </li> -->
    </ul>
  </div>
</template>

<script>
import { mapGetters,mapActions  } from "vuex";

export default {
  name: "Posts",
  computed: {
    ...mapGetters(["getAllPosts"])
  },
  methods: {
    ...mapActions(["getPostsAction", "removePostAction"])
  },
  created() {
    if(this.getAllPosts.length <= 0){
      this.getPostsAction();
    }
  }
};
</script>

<style scoped>
.list-group-item {
  color: brown;
}
</style>