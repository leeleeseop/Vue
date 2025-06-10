<script>
export default {

    // data(){
    //     return {
    //         click_yes : false
    //     }
    // },
    // methods: {
    //     createAlert() {
    //         if(this.click_yes){
    //             alert('경고창이 떴습니다.');
    //             this.click_yes = false;
    //         }
    //     }


    data() {
        return{
            kValue: ''
        }
    },
    methods: {
        getKey(e){
            this.kValue = e.key;
            //keydown.alt.s클릭할때
            alert('aler - s를 누르셨습니다.')
        }
    }
    
}
</script>

<template>

    <!-- <button v-on:click="createAlert">클릭해 보세요.</button> -->

    <!-- <button v-on:click.once="createAlert">클릭해 보세요.</button> -->

     <input type="text" v-on:keydown="getKey"><br>
     <span>{{ kValue }}</span><br>

    <!--s-->
     <input type="text" v-on:keydown.s="getKey"><br>
     <span>{{ kValue }}</span><br>

     <!--alt키 + s키 를 누르면 alert창이 출력 -->
     <input type="text" v-on:keydown.alt.s="getKey"><br>
     <span>{{ kValue }}</span><br>
</template>

<style></style>

.enter .tab .delete .esc .space .up .down. left. right .center
