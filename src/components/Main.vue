<template>
  <div class="container">
    <div class="row">
      <div class="left_side col-8">
        <Stories />
        <Posts />
      </div>
      <div class="right_side col-4">
        <div
          class="
            profile_big
            my-5
            p-5
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

        <div class="suggestion_for_you p-5">
          <div class="suggestions_top d-flex justify-content-between mb-5">
            <div class="suggestion_title text-secondary fw-bold">
              Suggerimenti per te
            </div>
            <div class="show_all fw-bold">Mostra Tutti</div>
          </div>

          <div
            class="
              suggestion
              d-flex
              justify-content-between
              align-items-center
              my-3
            "
          >
            <div class="profile_img profile_medium">
              <img src="../assets/profile.jpg" alt="" />
              <span class="fw-bold mx-3">Utente 1</span>
            </div>
            <div class="follow text-info">Segui</div>
          </div>

          <div
            class="
              suggestion
              d-flex
              justify-content-between
              align-items-center
              my-3
            "
          >
            <div class="profile_img profile_medium">
              <img src="../assets/profile.jpg" alt="" />
              <span class="fw-bold mx-3">Utente 1</span>
            </div>
            <div class="follow text-info">Segui</div>
          </div>

          <div
            class="
              suggestion
              d-flex
              justify-content-between
              align-items-center
              my-3
            "
          >
            <div class="profile_img profile_medium">
              <img src="../assets/profile.jpg" alt="" />
              <span class="fw-bold mx-3">Utente 1</span>
            </div>
            <div class="follow text-info">Segui</div>
          </div>

          <div
            class="
              suggestion
              d-flex
              justify-content-between
              align-items-center
              my-3
            "
          >
            <div class="profile_img profile_medium">
              <img src="../assets/profile.jpg" alt="" />
              <span class="fw-bold mx-3">Utente 1</span>
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

export default {
  components: {
    Stories,
    Posts,
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
</style>