<template>
  <main>
    
    <SectionConstruction />

    <SectionReferences />

    <SectionRecentWork />

    <SectionCoreValues />

    <SectionHomeOwners />

    <SectionLatestNews />

    <SectionPartners />

    <SectionBuildInspiring />
    
  </main>
</template>

<script>
import SectionConstruction from './SectionConstruction.vue';
import SectionReferences from './SectionReferences.vue';
import SectionRecentWork from './SectionRecentWork.vue';
import SectionCoreValues from './SectionCoreValues.vue';
import SectionHomeOwners from './SectionHomeOwners.vue';
import SectionLatestNews from './SectionLatestNews.vue';
import SectionPartners from './SectionPartners.vue';
import SectionBuildInspiring from './SectionBuildInspiring.vue';
export default {
  name: "MainComp",
  components: {
    SectionConstruction,
    SectionReferences,
    SectionRecentWork,
    SectionCoreValues,
    SectionHomeOwners,
    SectionLatestNews,
    SectionPartners,
    SectionBuildInspiring
  }
}
</script>

<style lang="scss" scoped>

</style>