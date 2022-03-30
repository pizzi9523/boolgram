<template>
  <div class="posts">
    <div class="post_card">
      <div
        class="top_post d-flex justify-content-between align-items-center px-5"
      >
        <div class="profile_post_author d-flex align-items-center">
          <div class="profile_post_img border">
            <img src="../assets/profile.jpg" alt="" />
          </div>
          <div class="profile_name mx-3 fw-bold">Ciccio</div>
        </div>

        <div class="menu_post">
          <i class="fa-solid fa-ellipsis fa-2x"></i>
        </div>
      </div>

      <div class="post_img">
        <img src="../assets/landscape.png" alt="" />
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
          <img src="../assets/profile.jpg" alt="" />
        </div>
        <div class="like_text mx-2">
          Piace a <span class="fw-bold">Ciccio</span> e altri
          <span class="fw-bold">34</span>
          <strong> persone</strong>
        </div>
      </div>
      <div class="post_description px-4 py-2">
        <span class="post_author fw-bold">Ciccio </span>
        <span class="post_title">Queen of Hearts.</span>
      </div>

      <div class="comments px-4">
        <div class="show_comments text-secondary">
          Mostra tutti e <span>4 </span> commenti.
        </div>
        <div class="comment">
          <span class="fw-bold comment_author">Autore Commento</span>
          <span class="comment_text"> I get* </span>.
        </div>
        <div class="comment">
          <span class="fw-bold comment_author">Autore Commento 2</span>
          <span class="comment_text"> ole* </span>.
        </div>
        <div class="comment">
          <span class="fw-bold comment_author">Autore Commento 3</span>
          <span class="comment_text"> ciao </span>.
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
export default {};
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

  .add_comment {
    border-top: 1px solid darkgrey;
    padding: 16px;
    input {
      border: 0;
      width: 80%;
    }
  }
}
</style>