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
            <p>SHOP</p>
            <ul>
              <li v-for="item in shop"><a href="#">{{item.label}}</a></li>
              
            </ul>
          </div>
          <div class="dc">
            <p>DC</p>
            <ul>
              <li v-for="item in dc"><a href="#">{{item.label}}</a></li>
            </ul>
          </div>
          <div class="sites">
            <p>SITES</p>
            <ul>
              <li v-for="item in sites"><a href="#">{{item.label}}</a></li>
            </ul>
          </div>
        </div>
        <div class="content-img">
          <img src="../assets/img/dc-logo-bg.png" alt="logo">
        </div>
      </div>
    </footer>
</template>

<style lang="scss">
footer {
  width: 100%;
  height: 250px;
  background-image: url('../assets/img/footer-bg.jpg');
}

.content-menu {
  display: flex;
}
</style>