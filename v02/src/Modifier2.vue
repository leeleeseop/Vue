<script>
    export default{
        data() {
            return{
                x: 0,
                y: 0,
                msg: ''
            }
        },
        methods: {
            mousePos(e) {
                this.x = e.offsetX;
                this.y = e.offsetY;
            },
            mouseClick(e) {
                //this.msg = this.x + ',' + this.y;

                //디폴드로 처리되는 것들을 막아준다 
                //e.preventDefault();
                
                // 마우스를 클릭하면 좌표가 누적되게 
                this.msg += this.x + ',' + this.y + "\n";
            }
        }
    }
</script>

<template>

    <!-- .right: 마우스 오른쪽 버튼을 클릭 했을때
         .prevent: 오른쪽 버튼을 클릭했을때 창이 안나오게 막아주는 수정자 -->
    <div id="display" v-on:mousemove="mousePos" v-on:click.right.prevent="mouseClick">
        x: {{ x }} <br>
        y: {{ y }}
    </div>
    <textarea>{{ msg }}</textarea>
</template>

<style>
    #display {
        width: 200px;
        height: 200px;
        background-color: goldenrod;
    }

    textarea {
        height: 500px;
    }
</style>
