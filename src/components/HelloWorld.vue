<template>
  <div v-if="comments.length !== 0">
    <div v-for="item in comments" :key="item.id" class="comment-item">
      {{ "name:" + item.name + "    id:" + item.id }}
      <HelloWorld :comments="item.children" />
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    comments: [],
  },
  created() {
    console.log(this.comments);
    console.log(this.comments.length);
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.comment-item {
  margin-left: 15px;
  text-align: left;
}
</style>
