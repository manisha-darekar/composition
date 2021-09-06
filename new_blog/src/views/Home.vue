<template>
  <div class="home">
   home
   <PostList v-if="showpost" :posts="posts"/>
   <button @click="showpost=!showpost">Toggle post</button>
   <button @click="posts.pop()">Delete Post</button>

  </div>
</template>

<script>
import PostList from '../components/PostList.vue'
import { ref } from '@vue/reactivity'


export default {
  name: 'Home',
  components:{PostList},
  setup(){
    const posts=ref([{title:'Blog for HTML',body:'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Voluptate, porro magnam aperiam aut aspernatur suscipit neque tempora hic exercitationem odio',id:1},
    {title:'blog for CSS',body:'css feature',id:2}])

    const showpost=ref(true)

    return{posts,showpost}
  }


   

   


    
}
</script>
