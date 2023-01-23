<script>
import SectionJumbo from './SectionJumbo.vue';
import SectionSmart from './SectionSmart.vue'
import SectionStats from './SectionStats.vue'
import SectionFeatures from './SectionFeatures.vue'
export default {
    components:{
        SectionJumbo,
        SectionSmart,
        SectionStats,
        SectionFeatures,
    }
}
</script>
<template lang="">
    <main>
        <SectionJumbo/>
        <SectionSectionSmart/>
        <SectionStats/>
        <SectionFeatures/>
    </main>
</template>
<style lang="scss" scoped>    
</style>