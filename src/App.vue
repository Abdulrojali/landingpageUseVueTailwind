<script>
import navigasiVue from './component/navigasi.vue';
import headingVue from './view/heading.vue'
import aboutVue from './view/about.vue'
import menuVue from './view/menu.vue'
import contactVue from './contact.vue'
import footerVue from './view/footer.vue';
export default{
  components:{
    navigasiVue,
    headingVue,
    aboutVue,
    menuVue,
    contactVue,
    footerVue
  }
}
</script>

<template>
  <div class="w-full h-full">
    <navigasiVue></navigasiVue>
    <headingVue></headingVue>
    <aboutVue></aboutVue>
    <menuVue></menuVue>
    <contactVue></contactVue>
    <footerVue></footerVue>
  </div>
</template>
<style>
.w-full{
  background-color:  black;
}
</style>