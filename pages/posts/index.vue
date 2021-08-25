<template>
  <b-container>
    <h1>post</h1>
    <Header />
    <b-row class="py-2">

      <PostContent />
      <PostContent />
      <PostContent />


    </b-row>
  </b-container>
</template>

<script>
import Header from '@/components/posts/Header'
import PostContent from '@/components/posts/PostContent'
export default {
  components: {
    Header,
    PostContent,
  },
}
</script>
