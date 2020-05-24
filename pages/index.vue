<template>
  <section id="posts">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :title="post.title"
      :excerpt="post.previewText"
      :thumbnailImage="post.thumbnailUrl"
      :id="post.id"
    />
  </section>
</template>

<script>
import PostPreview from "@/components/Blog/PostPreview";

export default {
  components: {
    PostPreview
  },
  data() {
    return {
      posts: [
        {
          title: "A new beginning",
          previewText: "This will bee askhjne jre jdaoso ner,we jr nfoasdjr",
          thumbnailUrl:
            "https://cdn.dribbble.com/users/1623562/screenshots/7009509/image.png",
          id: "a-new-beginning"
        },
        {
          title: "A second beginning",
          previewText: "This will bee askhjne jre jdaoso ner,we jr nfoasdjr",
          thumbnailUrl:
            "https://i.pinimg.com/736x/31/7f/30/317f3013293ec9b1aea5922548c1c664.jpg",
          id: "a-second-beginning"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
#posts {
  padding-top: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

@media (min-width: 35rem) {
  #posts {
    flex-direction: row;
  }
}
</style>