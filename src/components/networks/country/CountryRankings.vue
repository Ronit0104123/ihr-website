<script setup>
import GenericCardController from '@/components/controllers/GenericCardController.vue'
import CountryASRankings from '@/components/iyp/country/CountryASRankings.vue'

const props = defineProps(['countryCode', 'pageTitle'])
</script>

<template>
  <GenericCardController
    v-if="pageTitle"
    :title="$t('iyp.country.rankings.title')"
    :sub-title="$t('iyp.country.rankings.caption') + pageTitle"
    :info-title="$t('iyp.country.rankings.info.title')"
    :info-description="$t('iyp.country.rankings.info.description')"
  >
    <CountryASRankings :country-code="countryCode" :page-title="pageTitle" />
  </GenericCardController>
</template>

<style>
.card {
  margin-top: 20px;
}
</style>
