<script>
export default {
    data() {
        return{
            // 초기값 0 생성
            count: 0,
            Name: "이이섭",
            gender: "남자"
        }
    },
    methods: {
        clickAr : function() {
            this.Name = "이이섭";
            this.gender = "남자";
        }
    }
}
</script>

<template>
    <p>{{ "count : " + count}}</p>
    <!-- v-on:click="" : 클릭 이벤트를 처리하는 Vue디렉티브 클릭시 count++ count-- 실행 -> 카운드 값이 1씩 증가하거나 감소함함 -->
    <button v-on:click="count++">숫자증가</button>
    <button v-on:click="count--">숫자감소</button>
    
    <!-- v-on:mouseover="" : 마우스가 버튼 위로 올라갔을때 이벤트를 처리하는 vue디렉티브, count=0 : 마우스가
        올라와 있을때 값을 0으로 초기화 -->
    <button v-on:mouseover="count=0">0으로 초기화</button>

    <!-- v-on의 축약 : v-on:click = @click -->
    <button @click="clickAr">버튼</button>
</template>

<style>
</style>
