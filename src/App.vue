<script setup>
import '../assets/fonts/helvetica-neue/stylesheet.css'
import ConditionsComponent from '../components/ConditionsComponent.vue'
import DownloadComponent from '../components/DownloadComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'
import GiftsComponent from '../components/GiftsComponent.vue'
import HeaderComponent from '../components/HeaderComponent.vue'
import PrizesComponent from '../components/PrizesComponent.vue'
import RulesComponent from '../components/RulesComponent.vue'
</script>

<template>
  <HeaderComponent></HeaderComponent>
  <PrizesComponent></PrizesComponent>
  <RulesComponent></RulesComponent>
  <ConditionsComponent></ConditionsComponent>
  <DownloadComponent></DownloadComponent>
  <FooterComponent></FooterComponent>
  <GiftsComponent></GiftsComponent>
</template>

<style>
body {
  margin: 0 !important;
}
</style>
