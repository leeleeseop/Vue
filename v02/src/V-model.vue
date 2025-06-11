<script>
export default {
    data() {
        return {
            inputName : '이이섭2222',
            agree : false,
            itemName : null,
            itemCnt : 1,

            // 상품 목록 초기값
            sList : [
                { name: '감귤', cnt: 2}
            ]
        }
    },
    methods: {
        addItem() {
            let item = {
                name: this.itemName,
                cnt: this.itemCnt
            }
            // 상품목록에 추가
            this.sList.push(item);
            // 상품추가 후 품목과 수량 초기화 
            this.itemName = null;
            this.itemCnt = 1;
        }
    }
}
</script>

<template>
    
    <!-- 값을 바꾸면 {{ inputName }}의 값도 바뀐다.  -->
    <input type="text" v-model="inputName">
    <P>{{ inputName }}</P>

    <p>이 약관에 동의하십니까?</p>
    <input type="checkbox" v-model="agree"><br>
    {{ agree }}
    <!-- true면 가입하기 버튼태그가 보인다-->
    <button v-show="agree">가입하기</button>

    <form v-on:submit.prevent="addItem">
        <p>품목 : <input type="text" required v-model="itemName"></p>
        <p>수량 : <select v-model="itemCnt">
            <option value="1">1개</option>
            <option value="2">2개</option>
            <option value="3">3개</option>
            <option value="4">4개</option>
            <option value="5">5개</option>
        </select></p>
        <button type="submit">상품추가</button>
        <p>{{ itemName }} ({{ itemCnt }}개)</p>
    </form>
    <p>구입할 항목 :</p>
    <ul>
        <li v-for="item in sList">{{  item.name }} ({{ item.cnt }}개)</li>
    </ul>
</template>

<style>

</style>
