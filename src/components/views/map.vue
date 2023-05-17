<script>
import buttonView from '../Button.vue';
export default {
    components: {
        buttonView
    },
    data() {
        return {
            input: [
                {
                    name: '北部'

                },
                {
                    name: '中部'
                },
                {
                    name: '南部'
                },
                {
                    name: '東部'
                }
            ],
            isNorth: false,
            isSourth: false,
            isMid: false,
            isEast: false

        }
    },
    methods: {
        getCityIndex(index) {

            const northCity = document.querySelector(".img");

            console.log(index);


            if (index === 0) {
                this.isNorth = !this.isNorth;
            }else{
                this.isNorth =false;

            }
            if (index === 1) {
                this.isMid = !this.isMid;
            }else{
                this.isMid =false;

            }
            if (index === 2) {
                this.isSourth = !this.isSourth;
            }else{
                this.isSourth =false;

            }

            if (index === 3) {
                this.isEast = !this.isEast;
            }else{
                this.isEast =false;

            }

            // this.isNorth =! this.isNorth;

            // case "-":
            // num1=input1.value;//KEYIN進去一個自字串
            // i=parseInt(num1);
            // num2=input2.value;
            // j=parseInt(num2);
            // end=i-j;
            // break;

            // case "*":
            // num1=input1.value;//KEYIN進去一個自字串
            // i=parseInt(num1);
            // num2=input2.value;
            // j=parseInt(num2);
            // end=i*j;
            // break;

            // case "/":
            // num1=input1.value;//KEYIN進去一個自字串
            // i=parseInt(num1);
            // num2=input2.value;
            // j=parseInt(num2);
            // end=i/j;
            // break;



        }





    },
    // 生命週期
    mounted() {
        // this.fn();


    }
}




</script>


<template>
    <div class="bottom-layer">
        <div class="pic-layer">
            <img src="../../assets/img/683241228.jpg" alt="">
        </div>
        <div class="block">
            <div class="block-btn">
            <div class="topic">
                <p>選擇縣市</p>
            </div>
            <buttonView v-for="(item, index) in input" v-bind:district="item.name" @click="getCityIndex(index)" />
            </div>
            <div v-if="isNorth" class="img">
                <img src="../../assets/img/northDisplay.png" alt="">
            </div>
            <div v-if="isMid" class="img">
                <img src="../../assets/img/midDisplay.png" alt="">
            </div>
            <div v-if="isSourth" class="img">
                <img src="../../assets/img/southDisplay.png" alt="">
            </div>
            <div v-if="isEast" class="img">
                <img src="../../assets/img/EastDisplay.png" alt="">
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
.bottom-layer {


    .pic-layer {
        position: absolute;
        z-index: -1;
    }
}

.block {
    .topic {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    

    .block-btn{
    border: 2px solid #3d3a34;
    width: 12vw;
    height: 15vw;
    background: #d6caab;
    border-radius: 5px;
    position: fixed;
    top:30px;
    left:10px;
    z-index: 5;}
    

}

.img {
    width: 30vw;
    position: absolute;
    top: 0;
    left: 0;
    z-index: -1;
}

.hidden {
    display: none;
}</style>
