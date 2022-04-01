<template>
  <div class="posts">
    <div class="post_card" v-for="(post, index) in posts" :key="post.post_text">
      <div
        class="top_post d-flex justify-content-between align-items-center px-5"
      >
        <div class="profile_post_author d-flex align-items-center">
          <div class="profile_post_img border">
            <img :src="post.profile_picture" alt="" />
          </div>
          <div class="profile_name mx-3 fw-bold">
            {{ post.profile_fullname }}
          </div>
        </div>

        <div class="menu_post">
          <i class="fa-solid fa-ellipsis fa-2x"></i>
        </div>
      </div>

      <div class="post_img">
        <img :src="post.post_image" alt="" />
      </div>

      <div class="do_like_comment d-flex p-3">
        <div class="do_like mx-2">
          <i class="fa-regular fa-heart fa-2x"></i>
        </div>
        <div class="do_comment mx-2">
          <i class="fa-regular fa-comment fa-2x"></i>
        </div>
      </div>

      <div class="n_like px-4 d-flex">
        <div class="profile">
          <img
            v-if="post.likes.length > 0"
            :src="post.likes[post.likes.length - 1]['profile_picture']"
            alt=""
          />
        </div>
        <div class="like_text mx-2" v-if="post.likes.length > 0">
          Piace a
          <span class="fw-bold">{{
            post.likes[post.likes.length - 1]["username"]
          }}</span>
          e altri
          <span class="fw-bold">{{ post.likes.length }}</span>
          <strong> persone</strong>
        </div>
      </div>
      <div class="post_description px-4 py-2">
        <span class="post_author fw-bold">{{ post.profile_name }} </span>
        <span class="post_title">{{ post.post_text }}</span>
      </div>

      <div class="comments px-4">
        <div
          class="show_comments text-secondary"
          v-if="post.comments.length > 3"
          @click="showComments(index)"
        >
          Mostra tutti e <span>{{ post.comments.length }} </span> commenti.
        </div>
        <div v-if="comments_pointer == index">
          <div
            v-for="comment in post.comments"
            :key="comment['username']"
            class="comment"
          >
            <span class="fw-bold comment_author">{{ comment.username }}</span>
            <span class="comment_text"> {{ comment.text }} </span>
          </div>
        </div>
        <div v-else>
          <div
            v-for="comment in post.comments.slice(0, 3)"
            :key="comment['username']"
            class="comment"
          >
            <span class="fw-bold comment_author">{{ comment.username }}</span>
            <span class="comment_text"> {{ comment.text }} </span>
          </div>
        </div>
      </div>

      <div class="time_published p-4 text-secondary">33 ore fa.</div>

      <div class="add_comment d-flex justify-content-between">
        <input type="text" placeholder="Aggiungi un commento" />
        <div class="publish text-info">Pubblica</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      comments_pointer: null,
    };
  },
  props: {
    posts: Array,
  },
  methods: {
    showComments(index) {
      this.comments_pointer = index;
      // console.log(this.comments_pointer);
    },
  },

  mounted() {},
};
</script>

<style lang="scss">
.post_card {
  margin: 20px 0;
  .top_post {
    padding: 20px;

    .profile_post_author {
      .profile_post_img.border {
        background: linear-gradient(to right, red, purple) padding-box;
        border-radius: 50%;
        padding: 2px;
        border: 1px solid transparent;
        img {
          border: 3px solid white;
          border-radius: 50%;
          width: 50px;
          height: 50px;
        }
      }
    }
  }

  .post_img {
    img {
      width: 100%;
    }
  }

  .show_comments {
    &:hover {
      color: black !important;
      cursor: pointer;
    }
  }

  .add_comment {
    border-top: 1px solid darkgrey;
    padding: 16px;
    input {
      border: 0;
      width: 80%;
    }
  }

  .hidden {
    display: none;
  }
}
</style>