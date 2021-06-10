<template>
    <div>
        <Nav showBackArrow=true showText=true navText="醫療院所"></Nav>
        <div id="navbar">
            <div @click="ShowLeft=true" :class="{'press':ShowLeft, 'nonpress':!ShowLeft}">
                <div :class="{'show':ShowLeft, 'nonshow':!ShowLeft}">心理諮商</div>
            </div>
            <div @click="ShowLeft=false" :class="{'press':!ShowLeft, 'nonpress':ShowLeft}">
                <div :class="{'show':!ShowLeft, 'nonshow':ShowLeft}">精神醫療</div>
            </div>
        </div>

        <div v-if="ShowLeft">
            <div class="divide_bar"/>
                <div class="content" @click="openLink('https://health.tainan.gov.tw/page.asp?mainid={591C736A-19E9-453C-9CD6-DCF3E70AD417}')">
                    <div class="font_box">
                        <div class="title1">台南市衛生局 - 免費諮商服務</div>
                        <div class="title2">各區衛生所</div>
                    </div>
                    <div class="button">
                        <img src="@/assets/anson/0610/right_button.svg"></img>
                    </div>
                </div>
            </div>
        <div v-else>
            right
        </div>
    </div>
</template>

<style scoped rel="stylesheet" type="text/css">
#navbar{
    width: 100%;
    height: 7.4vh;
    background: linear-gradient(180deg, #F9FEA5 -214.29%, #96FBC4 -47.3%, #20E2D7 126.79%);
    box-shadow: 0 0.123vh 0 rgba(0, 0, 0, 0.1);

    display: flex;
    justify-content: space-around;
    align-items: center;
}
.press{
    background: #FFFFFF;
    border-radius: 1.23vh;
}
.show{
    width: 18.62vh;
    height: 4.69vh;
    display: flex;
    justify-content: center;
    align-items: center;

    font-family: Taipei Sans TC Beta;
    font-style: normal;
    font-weight: bold;
    font-size: 2.22vh;
    line-height: 4.19vh;
    background: linear-gradient(180deg, #F9FEA5 -214.29%, #96FBC4 -47.3%, #20E2D7 126.79%);
    -webkit-background-clip: text;
    background-clip: text;
    border-radius: 1.23vh;
    color: transparent;
}
.nonshow{
    width: 18.62vh;
    height: 4.69vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 2.22vh;
    background: none;
    border-radius: 1.23vh;

    font-family: Taipei Sans TC Beta;
    font-style: normal;
    font-weight: bold;
    font-size: 2.22vh;
    line-height: 4.19vh;
    color: rgba(255, 255, 255, 0.8);
}
.divide_bar{
    position: relative;
    width: 100vw;
    height: 0;
    top: 0.123vh;

    /*border: 0.2vh solid #A3FECC;*/
    border: 0.123vh solid rgba(163, 254, 204, 1)
}
.content{
    width: 100vw;
    height: 10.48vh;
    background: #FFFFFF;
    cursor: pointer;
    position: relative;
    
    display: flex;
    align-items: center;
}
.font_box{
    width: 36.13vh;
    padding: 0 0 0 2.96vh;
}
.button{
    position: relative;
    left: 2.96vh;
}
.title1{
    font-family: Taipei Sans TC Beta;
    font-style: normal;
    font-weight: normal;
    font-size: 2.22vh;
    color: #5C5C5C;
}
.title2{
    font-family: Taipei Sans TC Beta;
    font-style: normal;
    font-weight: normal;
    font-size: 1.85vh;
    color: #C7C7C7;
}
</style>

<script>
import Nav from '@/components/Nav.vue'

export default {
    name: 'Relax',
    components: {
        Nav
    },
    data() {
        return {
            ShowLeft: true,
        };
    },
    methods: {
        openLink: function(link) {
            window.open(link, '_blank');
        }
    }
}
</script>