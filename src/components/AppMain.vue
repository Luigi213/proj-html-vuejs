<script>
import SectionJumbo from './SectionJumbo.vue';
import SectionSmart from './SectionSmart.vue'
import SectionStats from './SectionStats.vue'
import SectionFeatures from './SectionFeatures.vue'
import SectionProcess from './SectionProcess.vue'
export default {
    components:{
        SectionJumbo,
        SectionSmart,
        SectionStats,
        SectionFeatures,
        SectionProcess,
    }
}
</script>
<template lang="">
    <main>
        <SectionJumbo/>
        <SectionSmart/>
        <SectionStats/>
        <SectionFeatures/>
        <SectionProcess/>
    </main>
</template>
<style lang="scss" scoped>    
</style>