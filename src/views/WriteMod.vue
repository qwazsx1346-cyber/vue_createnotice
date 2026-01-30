<script setup>
import { reactive, onMounted } from 'vue';
import { useRouter, useRoute } from 'vue-router';
import httpService from '@/services/httpService';

const route = useRoute();
const router = useRouter();

const rea = reactive({
    memo: {
        id: 0,
        title: '',
        contents: ''
    }
});

const submit = async () => {
    if(!rea.memo.title) {
        alert('제목을 입력해 주세요.');
        return;
    } else if(!rea.memo.contents) {
        alert('내용을 입력해 주세요.');
        return;
    }
}

onMounted(async () => {

}); 

</script>

<template>
<h3>글쓰기</h3>
<div>
    <label>제목<input type="text" v-model="rea.memo.title"></label>
</div>
<div>
    <label>내용<textarea v-model="rea.memo.contents"></textarea></label>
</div>
<div>
    <button @click="submit">저장</button>
</div>
</template>

<style scoped>

</style>