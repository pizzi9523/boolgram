<template>
  <div class="stories my-5 d-flex justify-content-between">
    <div
      class="storie_profile text-center mx-3"
      v-for="profile in profiles"
      :key="profile.profile_name"
    >
      <div class="border">
        <img :src="profile.profile_picture" alt="" />
      </div>
      <div class="name_profile">{{ profile.profile_name }}</div>
    </div>
    <!-- /storie_profile -->
  </div>
</template>

<script>
export default {
  props: {
    profiles: Array,
  },
};
</script>

<style lang="scss">
.stories {
  overflow: auto;
}
.storie_profile {
  .border {
    background: linear-gradient(to right, red, purple) padding-box;
    border-radius: 50%;
    padding: 3px;
    border: 2px solid transparent;
    width: fit-content;
    img {
      border: 4px solid white;
      border-radius: 50%;
      width: 75px;
      height: 75px;
    }
  }

  .name_profile {
    font-weight: bold;
    overflow: hidden;
    max-width: 74px;
    text-overflow: ellipsis;
  }
}
</style>