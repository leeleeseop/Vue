<script>
export default{

    /*data: function*/
    data(){
        return{

            /*channel이란 변수에 "이이섭 vue로 홈페이지 만들기" 담고
              subscribe 값에 2677담는다
            */
            channel : "이이섭 vue로 홈페이지 만들기",
            subscribe: 2677,
        }
    },
};
</script>

<template>

    <!--{{ }} = 코스형문법 머스태쉬-->
    <h1>채널명: {{ channel }}</h1>
    <h2>구독자수: {{ subscribe }}</h2>
    <!-- <P>{{'오늘의 행운 숫자 :' + Math.ceil(Mat.random() * 45)}}</P> -->
    <P>오늘의 행운 숫자 : {{Math.ceil(Math.random() * 45)}}</P>

</template>

<style scoped></style>