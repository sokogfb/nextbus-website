<template lang="pug">
  nav
    .logo
      nuxt-link(to="/")
        img(src='~/assets/svg/logo.svg')
    .right
      //- nuxt-link(to="") Blog
      nuxt-link(to="/guides") Guides
      nuxt-link(to="/#features").highlight.features Features
      nuxt-link(to="/#download").highlight.install Download
</template>

<script>
export default {
}
</script>

<style lang="scss" scoped>
nav {
  background-color: rgb(248, 248, 248);
  border-bottom: 1px solid rgb(230, 230, 230);
  display: flex;

  justify-content: space-between;
  align-items: center;

  padding: calc(var(--dense-padding) * 1.5) var(--main-padding);

  position: sticky;
  top: 0;

  .logo {
    img {
      height: calc(var(--font-size) * 2);
    }
  }

  font-size: 0.8em;

  .right {
    display: flex;
    align-content: center;

    & > a {
      // margin-left: var(--main-padding);

      display: block;

      color: unset;
      text-decoration: unset;

      padding: var(--dense-padding) calc(var(--dense-padding) * 3.5);
      line-height: 1.8;

      &.highlight {
        // background-color: rgb(200, 200, 200);
        background-color: rgba(0, 0, 0, .05);

        &.features {
          border-radius: 9px 0 0 9px
        }
        &.install {
          background-color: rgba(0, 0, 0, .15);
          border-radius: 0 9px 9px 0;
        }
      }
    }
  }
}
</style>