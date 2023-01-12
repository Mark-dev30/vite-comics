<script>

export default {
  name: "AppFooter",
  data() {
    return {
      comics: [
        { label: 'Characters' }, { label: 'Comics' }, { label: 'Movies' }, { label: 'Tv' }, { label: 'Games' }, { label: 'Videos' }, { label: 'News' }
      ],
      shop: [
        { label: 'Shop DC' }, { label: 'Shop DC Collectibles' }
      ],
      dc: [
        { label: 'Term Of Use' }, { label: 'Privacy policy (New)' }, { label: 'Ad Choices' }, { label: 'Advertising' }, { label: 'Jobs' }, { label: 'Subscriptions' }, { label: 'Talent Workshops' }, { label: 'CPSC Certigicates' }, { label: 'Ratings' }, { label: 'Shop Help' }, { label: 'Contact Us' },
      ],
      sites: [
        { label: 'DC' }, { label: 'MAD Magazine' }, { label: 'DC Kids' }, { label: 'DC Universe' }, { label: 'DC Power Visa' }
      ],

      img_social: [
        { image: 'footer-facebook.png' }, { image: 'footer-twitter.png' }, { image: 'footer-youtube.png' }, { image: 'footer-pinterest.png' }, { image: 'footer-periscope.png' }
      ]

    }
  }
}
</script>
<template lang="">
    <footer>
      <div class="container-footer">
        <div class="content-menu">
          <div class="dc-shop">
            <p>DC COMICS</p>
            <ul>
                <li v-for="item in comics"><a href="#">{{item.label}}</a></li>
            </ul>
            <p class="shop">SHOP</p>
            <ul>
              <li v-for="item in shop"><a href="#">{{item.label}}</a></li>
              
            </ul>
          </div>
          <div class="dc margin-20">
            <p>DC</p>
            <ul>
              <li v-for="item in dc"><a href="#">{{item.label}}</a></li>
            </ul>
          </div>
          <div class="sites margin-20">
            <p>SITES</p>
            <ul>
              <li v-for="item in sites"><a href="#">{{item.label}}</a></li>
            </ul>
          </div>
        </div>
      </div>
      <div class="container-social">
        <div class="row-social">
            <div class="sign-up">
              <button class="sign-btn">SIGN-UP NOW!</button>
            </div>
            <div class="social">
              <h4>FOLLOW US</h4> 
              <ul>
                <li v-for="img in img_social">
                  <a href="#">
                    <img :src="`src/assets/img/${img.image}`">
                  </a>
                </li>
              </ul>
            </div>
        </div>
      </div>
    </footer>
</template>

<style lang="scss">
@use '../styles/partials/variables' as *;

footer {
  width: 100%;
  background-image: url('../assets/img/footer-bg.jpg');
}

.container-footer {
  width: 80%;
  margin: 0 auto;
  background-image: url(../assets/img/dc-logo-bg.png);
  background-repeat: no-repeat;
  background-position: right center;

  .content-menu {
    display: flex;
    padding: 30px;

    .shop {
      margin-top: 20px;
    }

    p {
      color: white;
    }

    li {
      list-style: none;

      a {
        text-decoration: none;
        color: grey;
      }
    }
  }
}

.container-social {
  width: 100%;
  height: 70px;
  background-color: #303030;

  .row-social {
    width: 80%;
    height: 100%;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
}

.sign-btn {
  border: 2px solid $color_blue;
  background-color: transparent;
  color: white;
  padding: 8px;
  cursor: pointer;
}

.social {
  display: flex;
  align-items: center;

  li {
    list-style: none;
    display: inline-block;
    margin: 10px;
  }

  h4 {
    color: $color_blue;
  }
}

.margin-20 {
  margin-left: 20px;
}
</style>