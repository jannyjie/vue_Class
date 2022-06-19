<template>
  <div>
    <h3>Edit Post</h3>
    <form @submit.prevent="onSubmit">
     <div class="mb-3">
        <label for="eid" class="form-label"> Id</label>
        <input type="text" class="from-control" id="eid" v-model="form.id" disabled/>
      </div>
      <div class="mb-3">
        <label for="uid" class="from-label">User Id</label>
        <input type="text" class="from-control" id="uid" v-model="form.userId" />
      </div>
      <div class="mb-3">
        <label for="uid" class="from-label">User title</label>
        <input type="text" class="from-control" id="uid" v-model="form.title" />
      </div>
      <div class="bt-3">
        <label for="uid" class="from-label">Body</label>
        <input type="text" class="from-control" id="body" v-model="form.body" />
      </div>
      <button type="submit" class="btn btn-prmary">Submit</button>
    </form>
  </div>
</template>

<script>
import {mapActions, mapState} from 'vuex'
export default {
  name:"EditPost",
  methods:{
    ...mapActions(["editPostAction"]),
    onSubmit(){
      this.editPostAction(this.form);
      this.$router.push("/");
    }
  },
  data(){
    return{
      form:{
      }
    }
  },
  computed:{
    ...mapState(["posts"])
  },
  mouthed(){
    const rid = Number.parseInt(this.$route.params.id),
    ar = this.posts,
    p = ar.find(o => o.id == rid)
    this.form = p
  }
}
</script>

<style>

</style>