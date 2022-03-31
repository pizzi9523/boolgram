<template>
  <div class="container">
    <div class="row">
      <div class="left_side col-8">
        <Stories :profiles="this.profiles" />
        <Posts :posts="this.posts" />
      </div>
      <div class="right_side col-4">
        <div
          class="
            profile_big
            my-5
            px-5
            d-flex
            justify-content-between
            align-items-center
          "
        >
          <div class="profile_img">
            <img src="../assets/profile.jpg" alt="" />
          </div>

          <div class="profile_name">
            <div class="nickname fw-bold">Ciccio_ciccio</div>
            <div class="name">Ciccio Ciccio</div>
          </div>

          <div class="pass text-info">Passa a</div>
        </div>

        <div class="suggestions_top d-flex justify-content-between mb-2 px-5">
          <div class="suggestion_title text-secondary fw-bold">
            Suggerimenti per te
          </div>
          <div class="show_all fw-bold">Mostra Tutti</div>
        </div>
        <div class="suggestion_for_you px-5">
          <div
            class="
              suggestion
              d-flex
              justify-content-between
              align-items-center
              my-3
            "
            v-for="profile in this.profiles"
            :key="profile.profile_name"
          >
            <div class="profile_img profile_medium">
              <img :src="profile.profile_picture" alt="" />
              <span class="fw-bold mx-3">{{ profile.profile_name }}</span>
            </div>
            <div class="follow text-info">Segui</div>
          </div>
        </div>

        <footer>
          <div class="p-4">
            <span class="text-secondary">
              &copy; 2022 BOOLGRAM FROM GIUSEPPE PIZZITOLA</span
            >
          </div>
        </footer>
      </div>
    </div>
  </div>
  <!-- /.container -->
</template>

<script>
import Stories from "../components/Stories.vue";
import Posts from "../components/Posts.vue";
import axios from "axios";

export default {
  data() {
    return {
      api_uri_profiles:
        "https://flynn.boolean.careers/exercises/api/boolgram/profiles",
      api_uri_posts:
        "https://flynn.boolean.careers/exercises/api/boolgram/posts",
      profiles: [],
      posts: [],
    };
  },
  components: {
    Stories,
    Posts,
  },

  mounted() {
    axios
      .get(this.api_uri_profiles)
      .then((response) => {
        // console.log(response.data);
        this.profiles = response.data;
        console.log(this.profiles);
      })
      .catch((e) => {
        console.log(e, "ERROR");
      });

    axios
      .get(this.api_uri_posts)
      .then((response) => {
        this.posts = response.data;
        console.log(this.posts);
        // response.data.forEach((post) => {
        //   console.log(post.likes.length);
        // });
      })
      .catch((e) => {
        console.log(e, "ERROR");
      });
  },
};
</script>

<style lang="scss">
@import "../assets/scss/common.scss";
.left_side {
  .stories {
    border: 1px solid darkgray;
    padding: 50px;
  }

  .posts {
    .post_card {
      border: 1px solid darkgray;
    }
  }
}

.right_side {
  position: fixed;
  right: 50px;
  top: 72px;
  overflow: auto;
  transform: scale(0.9);
  .suggestion_for_you {
    height: 335px;
    overflow: hidden;
  }
}
</style>