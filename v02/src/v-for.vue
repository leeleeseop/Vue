<script>
    export default {
        data(){
            return {
                sports: [
                    'Baseball',
                    'Football',
                    'Volleyball',
                    'Swimming'
                ]
            }
        }
    }
</script>

<template>
    <ul>
        <!--sports에서 값을 받아서 sport에 하나씩 값을 담는다 -->
        <li v-for="sport in sports">{{ sport }}</li>

        <!--index를 추가해서 스포츠 앞에 인덱스 번호도 같이 출력-->
        <li v-for="(sport, index) in sports">{{ index }} {{ sport }}</li>

        <!--+1를 추가해서 0123이 아닌 1부터 시작 -->
        <li v-for="(sport, index) in sports">{{ index + 1 }} {{ sport }}</li>
    </ul>
</template>

<style></style>
