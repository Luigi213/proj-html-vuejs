<script>
import SectionJumbo from './SectionJumbo.vue';
import SectionSmart from './SectionSmart.vue'
import SectionStats from './SectionStats.vue'
import SectionFeatures from './SectionFeatures.vue'
import SectionProcess from './SectionProcess.vue'
import SectionMember from './SectionMember.vue'
import SectionClients from './SectionClients.vue'
import SectionRegister from './SectionRegister.vue';
export default {
    components:{
        SectionJumbo,
        SectionSmart,
        SectionStats,
        SectionFeatures,
        SectionProcess,
        SectionMember,
        SectionClients,
        SectionRegister
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
        <SectionMember/>
        <SectionClients/>
        <SectionRegister/>
    </main>
</template>
<style lang="scss" scoped>    
</style>