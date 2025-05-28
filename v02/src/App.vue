<script>
export default{
    /*data: function*/
    data(){
        return{

            /*
              channel이란 변수에 "이이섭 vue로 홈페이지 만들기" 담고
              subscribe 값에 2677담는다
            */
            page: "이이섭 vue로 홈페이지 만들기",
            subscribe: 2677,
            test: "test01",
            score : false,
            score1 : 65,
            score2 : false
        }
    },
};
</script>

<template>
    <!--2025-05-28 Text Interpolation-->
    <!--{{ }} = 코스형문법 Mustache 태그-->
    <h1>페이지명:{{ page }}</h1>
    <h2>구독자수:{{ subscribe }}</h2>
    <!-- <P>{{'오늘의 행운 숫자 :' + Math.ceil(Mat.random() * 45)}}</P> -->
    <P>오늘의 행운 숫자 : {{Math.ceil(Math.random() * 45)}}</P>

    <!-- 2025-05-28 Directives(디렉티브) -->
    <!-- 태그안에 값을 넣으면 안된다 -->
    <p v-html="test"></p>
    <h2 v-text="subscribe"></h2>

    <!--v-pre를 넣으면 채널명이 아니라 태그 안에 내용이 출력-->
    <h1 v-pre>채널명: {{ page }}</h1>

    <!-- v-if: 참이면 출력이 되고 거짓이면 출력이 되지 않는다. -->
    <h1 v-if="score">이 부분이 출력됩니다.</h1>
    <!-- v-if else 사용 v-if는 단독으로 사용이 가능하지만 
        else가 붙어있으면 v-if가 있어야한다. -->
    <h1 v-if="score1 >= 90">평점 : A</h1>
    <h1 v-else-if="score1 >= 80">평점 : B</h1>
    <h1 v-else-if="score1 >= 70">평점 : C</h1>
    <h1 v-else>평점 : F</h1>

    <h1 v-if="score2 != 60">이 여역은 v-if에서 처리하고 있습니다.</h1>

    <!--반복적으로 나타났다 사라져야 되는 토글이 되거나
    엘리먼트의 표시여부를 조건에 보이게 하거나 숨기는 역할  -->
    <h1 v-show="score2">이 여역은 v-show에서 처리하고 있습니다.</h1>
</template>

<style scoped></style>
