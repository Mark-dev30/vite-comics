<script>
import AppHeader from './components/AppHeader.vue'
import AppContain from './components/AppContain.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  components: {
    AppHeader,
    AppContain,
    AppFooter
  }

}
</script>
<template lang="">
  <div >
    <AppHeader></AppHeader>
    <AppContain></AppContain>
    <AppFooter></AppFooter>
  </div>
</template>

<style lang="scss">
@use './styles/generals.scss' as *;
</style>
