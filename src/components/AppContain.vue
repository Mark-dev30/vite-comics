<script>
import AppCard from './AppCard.vue';

export default {
  name: "AppContain",
  components: {
    AppCard
  },
  data() {
    return {
      thumbs: [
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          "price": "$19.99",
          "series": "Action Comics",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          "price": "$3.99",
          "series": "American Vampire 1976",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          "price": "$16.99",
          "series": "Aquaman",
          "type": "graphic novel"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          "price": "$2.99",
          "series": "Batgirl",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          "price": "$3.99",
          "series": "Batman",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          "price": "$2.99",
          "series": "Batman Beyond",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          "price": "$3.99",
          "series": "Batman/Superman",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          "price": "$4.99",
          "series": "Batman/Superman Annual",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          "price": "$5.99",
          "series": "Batman: The Joker War Zone",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          "price": "$6.99",
          "series": "Batman: Three Jokers",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          "price": "$4.99",
          "series": "Batman: White Knight Presents: Harley Quinn",
          "type": "comic book"
        },
        {
          "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          "price": "$16.99",
          "series": "Catwoman",
          "type": "graphic novel"
        }
      ]
    }
  }
}
</script>
<template lang="">
    <main>
      <div class="jumbotron"></div>
      <div class="container-cards">
          <div class="content-cards">
              <AppCard v-for="(thumb, index) in thumbs" :key="index" :card="thumb"></AppCard> 
          </div>
          <div class="content-btn">
            <button class="more-btn">LOAD MORE</button>
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

.jumbotron {
  width: 100%;
  height: 300px;
  background-image: url(../assets/img/jumbotron.jpg);
  background-size: cover;
}

.container-cards {
  width: 100%;
  background-color: #1c1c1c;
  padding: 1rem 0;
}

.content-cards {
  width: 80%;
  margin: 0 auto;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.container-link {
  width: 100%;
  height: 100px;
  background-color: $color_blue;
  display: flex;
  align-items: center;

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

      span {
        text-transform: uppercase;
        color: white;
        margin-left: 10px;
        font-size: 15px;
      }
    }

  }
}

.content-btn {
  margin-top: 30px;
  text-align: center;

  .more-btn {
    color: white;
    font-size: 12px;
    padding: 8px 30px;
    background-color: $color_blue;
    border: none;
  }
}
</style>