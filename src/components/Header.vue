<template>
  <header class="full-width">
      <div class="header container debug px-15">
          <div class="header-logo">
              <img src="../assets/logo_seo_w_1x.png" alt="">
          </div>
          <nav class="header-link debug">

          </nav>
          <div class="header-button">
              <button class="button-primary">Get in touch now</button>
          </div>
      </div>
  </header>
</template>

<script>
export default {
    name: 'Header'
}
</script>

<style scoped lang="scss">
.header {
    height: 100px;
    display: flex;
    .header-logo {
        height: 100%;
        display: flex;
        align-items: center;
    }
    .header-link {
        flex-grow: 1;
    }
    .header-button {
        display: flex;
        align-items: center;
    }
}

</style>