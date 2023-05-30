<script>
import PageHeader from './components/PageHeader.vue'
import PageMain from './components/PageMain.vue'
import PageFooter from './components/PageFooter.vue'

export default {
  name: "App",
  components: {
    PageHeader,
    PageMain,
    PageFooter
  },
  data() {
    return {
    }
  },
  mounted() {
  },
  methods: {
  }
}
</script>

<template>
  <PageHeader 
    textButton=     "ORDER ONLINE"
    :middleNavList= "[['HOME', '../src/assets/svg/svg-0.svg'],
                      'PAGES',
                      'MENU',
                      'EVENT',
                      'BLOG',
                      'LANDING']"
    :sideNavList=   "[['CART', '../src/assets/svg/svg-1.svg']]"
    logoPath="../src/assets/img/h5-logo-divided-header.png"
    :headerHeight="130"
  />
  <PageMain />
  <PageFooter />
</template>

<style lang="scss" scoped>
</style>
