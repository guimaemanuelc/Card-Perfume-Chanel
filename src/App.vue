<template>
  <main class="[ content ][ flex ]" data-type="column">
    <div class="[ content_card ]">
      <router-view />
   </div>
  </main>
</template>

<script>
export default {
  name: "App",
};
</script>

<style lang="scss">
.content {
  align-items: center;
  justify-content: center;
  height: 100vh;
  background: var(--cream);

  &_card {
    width: 550px;
    height: 450px;
  }

  @media only screen and (max-width: 428px) {
    .content_card{
      width: 350px;
      height: auto;
    }
  }
}
</style>