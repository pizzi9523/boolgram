<template>
  <div class="container">
    <div class="row">
      <div class="left_side col-8">
        <div class="stories text-center mt-5">
          <img class="mb-2" src="../assets/spinner.gif" alt="" />
          <div class="d-flex justify-content-between">
            <div
              class="storie_profile text-center mx-3"
              v-for="profile in 6"
              :key="profile"
            >
              <div class="storie_skeleton"></div>
            </div>
            <!-- /storie_profile -->
          </div>
        </div>
        <div class="posts">
          <div class="post_card">
            <div
              class="
                top_post
                d-flex
                justify-content-between
                align-items-center
                px-5
              "
            >
              <div class="profile_post_author d-flex align-items-center">
                <div class="profile_post_img_skeleton profile_medium"></div>
                <div class="profile_name_skeleton mx-3 fw-bold"></div>
              </div>

              <div class="menu_post">
                <i class="fa-solid fa-ellipsis fa-2x"></i>
              </div>
            </div>

            <div
              class="
                post_img_skeleton
                d-flex
                justify-content-center
                align-items-center
              "
            >
              <img
                width="50px"
                height="50px"
                src="../assets/spinner.gif"
                alt=""
              />
            </div>
          </div>
        </div>
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
            v-for="profile in 6"
            :key="profile"
          >
            <div
              class="
                profile_img profile_medium
                d-flex
                align-items-center
                justify-content-between
              "
            >
              <div class="profile_post_img_skeleton"></div>
              <span class="profile_name_skeleton mx-5"></span>
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
export default {};
</script>

<style lang="scss">
.skeleton {
  .profile_post_img_skeleton {
    border: 2px solid lightgrey;
    background-color: lightgrey;
    height: 50px;
    width: 50px;
    border-radius: 50%;
    display: inline-block;
  }

  .profile_name_skeleton {
    width: 150px;
    height: 20px;
    background: linear-gradient(45deg, white, lightgrey);
    animation-name: expand;
    animation-duration: 5s;
  }

  .storie_skeleton {
    border-radius: 50%;
    padding: 3px;
    border: 2px solid lightgrey;
    background-color: lightgrey;
    width: 75px;
    height: 75px;
  }

  .post_img_skeleton {
    width: 100%;
    height: 854px;
  }

  @keyframes expand {
    0% {
      background: linear-gradient(90deg, white, lightgrey);
      width: 20px;
    }

    50% {
      background: linear-gradient(90deg, white, lightgrey);
      width: 75px;
    }

    100% {
      background: linear-gradient(90deg, white, lightgrey);
      width: 150px;
    }
  }
}
</style>