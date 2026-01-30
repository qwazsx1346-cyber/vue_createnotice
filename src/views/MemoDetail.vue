<script setup>
import { reactive, onMounted  } from 'vue';
import { useRoute, useRouter } from 'vue-router';
import httpService from '@/services/httpService';

const route = useRoute();
const router = useRouter();

const rea = reactive({
    data: {
        id: 0,
        title: '',
        contents: '',
        createAt: ''
    }
});

onMounted(async () => {

});
</script>

<template>

</template>

<style scoped>

</style>