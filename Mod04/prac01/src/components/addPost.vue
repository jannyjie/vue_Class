<template>
  <div>
    <h3>Add Post</h3>
    <form @submit.prevent="onSubmit">
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
import {mapActions} from 'vuex'
export default {
  name:"AddPost",
  methods:{
    ...mapActions(["addPostAction"]),
    onSubmit(){
      console.log(2);
      this.addPostAction(this.form);
      this.form ={
        userId: '',
        title: "",
        body:""
      };
    }
  },
  data(){
    return{
      form:{
        userId:"",
        title:"",
        body:""
      }
    }
  }
}
</script>

<style>

</style>