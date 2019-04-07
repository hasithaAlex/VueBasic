<template>
    <div>
        <app-status v-for="status in 5" :key="status"></app-status>
    </div>
</template>

<script>
    import ServerStatus from './ServerStatus.vue';
    export default {    
        components: {
            'app-status': ServerStatus 
        }
    }
</script>