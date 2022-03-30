<template>
  <nav class="Navbar py-4">
    <div class="container px-3">
      <div class="d-flex justify-content-between align-items-center">
        <div class="logo">
          <a href="#">
            <img src="../assets/logo.png" alt="" />
          </a>
        </div>
        <!-- /logo  -->

        <div class="search">
          <input type="text" name="search" id="searchbar" placeholder="Cerca" />
        </div>
        <!-- /search  -->

        <div class="menu d-flex">
          <div class="followed px-2">
            <a href="#">
              <i class="fa-regular fa-heart"></i>
            </a>
          </div>
          <div class="home px-2">
            <a href="#">
              <i class="fa-solid fa-house-chimney"></i>
            </a>
          </div>
          <div class="profile px-2">
            <a href="#">
              <img src="../assets/profile.jpg" alt="" />
            </a>
          </div>
        </div>
        <!-- /menu  -->
      </div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style lang="scss">
.Navbar {
  border-bottom: 1px solid darkgray;
  a {
    color: black;
    text-decoration: none !important;
    i {
      width: 24px;
    }
  }

  .logo {
    img {
      width: 103px;
    }
  }

  .search {
    input {
      padding: 0 10px;
      border: 1px solid lightgray;
      &::placeholder {
        color: darkgray;
        text-align: center;
      }
    }
  }
  .menu {
    align-items: center;
    .profile {
      img {
        width: 24px;
        border-radius: 50%;
      }
    }
  }
}
</style>