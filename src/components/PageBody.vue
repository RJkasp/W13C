
<template>
<!-- pageBody having playList being injected into it -->
    <div id="pageBody">
       <play-list></play-list>
    </div>
</template>

<script>
import PlayList from './PlayList.vue'
    export default {
        name: 'page-body',
        components:{
            PlayList,
        }
    }
</script>

<style scoped>

</style>