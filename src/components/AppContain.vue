<script>

export default {
  name: "AppContain",
  data() {
    return {

    }
  }
}
</script>
<template lang="">
    <main>
      <div class="container-title">
          <div class="title">
            <h3> -- Content goes here -- </h3>
          </div>
      </div>
      <div class="container-link">
        <div class="content-link">
          <div class="link">
            <img src="../assets/img/buy-comics-digital-comics.png" alt="digital-comics">
            <span>digital comics</span>
          </div>
          <div class="link">
            <img src="../assets/img/buy-comics-merchandise.png" alt="merchandise-comics">
            <span>merchandise-comics</span>
          </div>
          <div class="link">
            <img src="../assets/img/buy-comics-subscriptions.png" alt="subscriptions-comics">
            <span>subscriptions</span>
          </div>
          <div class="link">
            <img src="../assets/img/buy-comics-shop-locator.png" alt="shop-locator">
            <span>comic shop locator</span>
          </div>
          <div class="link">
            <img src="../assets/img/buy-dc-power-visa.svg" alt="dc-power">
            <span>dc power visa</span>
          </div>
        </div>

      </div>
    </main>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;

.container-title {
  width: 100%;
  height: 100px;
  background-color: black;
  display: flex;
  align-items: center;

}

.title {
  width: 80%;
  margin: 0 auto;

  h3 {
    color: white;
  }

}




.container-link {
  width: 100%;
  background-color: $color_blue;

  .content-link {
    display: flex;
    justify-content: space-between;
    width: 80%;
    margin: 0 auto;

    .link {
      display: flex;
      align-items: center;

      img {
        width: 50px;
        height: 50px;
        object-fit: contain;

      }
    }

  }
}
</style>