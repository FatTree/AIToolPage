<script setup>

</script>

<template>
  <div class="footer MaxW">
    <div class="footer__left">
      <span>AI工具王 © 2023</span>
      <div class="links">
        <a href="" class="socialLink">Facebook</a>
        <a href="" class="socialLink">Twitter</a>
        <a href="" class="socialLink">Instagram</a>
      </div>
    </div>
    <a href="" class="socialLink">
      Back to top
      <span class="material-icons">
        <span class="material-symbols-outlined">arrow_upward</span>
      </span>
    </a>
  </div>
</template>

<style lang="scss" scoped>
@import '../assets/main.module.scss';
.footer {
  display: flex;
  justify-content: space-between;
  padding: 10px 0;
  @include TC-Font(16px, 1.5, $Black);
  font-weight: $Blob-FW;

  a {
    color: $Black0;
  }

  &__left {
    display: flex;
    > .links {
      padding-left: 100px;

      > .socialLink {
        padding-right: 20px;
      }
    }
  }

}
</style>
