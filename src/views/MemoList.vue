<script setup>
import { reactive, onMounted } from 'vue';
import { useRouter, useRoute } from 'vue-router';
import httpService from '@/services/httpService';

const route = useRoute();
const router = useRouter();

const rea = reactive({
    list: []
});

onMounted(async () => {

});

// const moveToDetail = id => {
//   router.push(path: '/')
// }

</script>

<template>
<h3>게시판 리스트</h3>
<table>
    <tr>
      <th>번호</th>
      <th>제목</th>
      <th>작성일</th>
    </tr>
    <tr v-for="item in rea.list" :key="item.id" @click="moveToDetail(item.id)">
        <td>{{ item.id }}</td>
        <td>{{ item.title }}</td>
        <td>{{ item.createdAt }}</td>
    </tr>
</table>
</template>

<style scoped>

</style>