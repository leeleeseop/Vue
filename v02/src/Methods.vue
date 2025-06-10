<!-- methods 만들어 사용자 이름출력과 함수 증감 -->

<script>
export default {

    // 데이터 옵션
    //data: function
    /**
    data() {
        return{
            userName : '이이섭'
        }
    },
     */

    // methods: {
        //외부에서 userName을 전달받는다.
    //  greeting(userName) {
            //userName을 합칠때 this.를 넣어야 한다.
            //userName을 받아서 this.를 사용하지 않고 userName을 사용
    //         return ' Hi, there' + userName
    //     }
    // },

    data(){
        return {
            num: 0
        }
    },
    methods: {
        increment(){
            this.num++
        },
        decrement() {
            this.num--
        }
    }
}
</script>

<template>
    <!--'이이섭'이라는 문자열을 인자에 넘긴다-->
    <!-- <h1>{{ greeting('이이섭') }}</h1> -->

    <p>{{ num }}</p>
    <!-- num++ 과 num-- 직접 증가 감소를 했지만 메서드를 호출하는 방식으로 숫자를 증감 -->
    <button v-on:click="increment">Increase number</button>
    <button v-on:click="decrement">Decrease number</button>
</template>

<style></style>
