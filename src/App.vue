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
      footerInfo: {
        textListCol1:[
          [
            "1614 E. Bell Rd #104",
            "Salerno, AZ 85022",
            "(602) 867-1010"
          ],
          [
            "204 E. Pizzetta Tommaso",
            "Sorrento, AZ 85022",
            "(358) 867-1010"
          ],
          [
            "Vale Puglia 54",
            "Torre Del Greco, AZ 85022",
            "(359) 867-1010"
          ],
          [
            "Corso Itali AA",
            "Naples, AZ 85022",
            "(989) 867-1010"
          ]
        ],
        textListCol2:[
          {
            title: "MONDAY",
            info: "Kitchen Closed",
            dangerInfo: true
          },
          {
            title: "TUESDAY UNTIL FRIDAY",
            info: "9:00 - 22:00",
            dangerInfo: false
          },
          {
            title: "SATURDAY",
            info: "Saturday 11am to midnight",
            dangerInfo: false
          },
          {
            title: "SUNDAY",
            info: "9:00 - 22:00",
            dangerInfo: false
          }
        ],
        textCol3: "THE DON PEPPE CREW FIRST AND FOREMOST VALUES AN AUTHENTIC, WELL BAKED SLICE OF PIZZA."
      }
    }
  },
  mounted() {
  },
  methods: {
  }
}
</script>

<template>
  <PageHeader textButton="ORDER ONLINE" :middleNavList="[['HOME', '/assets/svg/svg-0.svg'],
    'PAGES',
    'MENU',
    'EVENT',
    'BLOG',
    'LANDING']" :sideNavList="[['CART', '/assets/svg/svg-1.svg']]"
    logoPath="/assets/img/h5-logo-divided-header.png" :headerHeight="130" />
  <PageMain />
  <PageFooter :textListCol1="footerInfo.textListCol1" :textListCol2="footerInfo.textListCol2" :textCol3="footerInfo.textCol3"/>
</template>

<style lang="scss" scoped></style>
