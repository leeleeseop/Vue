<script>
export default {

    data(){
        return {
            click_yes : false
        }
    },

    methods: {
        createAlert() {
            if(this.click_yes){
                alert('경고창이 떴습니다.');
                this.click_yes = false;
            }
        }
    }
}

</script>

<template>
    <button v-on:click="createAlert">클릭해 보세요.</button>
</template>

<style></style>
