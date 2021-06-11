<template>
    <div>
        <Nav showBackArrow=true showText=true navText="讀讀文章"></Nav>
        <div id="layout">
            <div v-if="content==0">
                content0
                <div class="title" v-text="main[0].title"></div>
                <div class="author" v-text="main[0].author"></div>
                <div class="pic_box"><img style="height:19.96vh" src="@/assets/anson/0610/c0p0.png"></img></div>
                <div v-text="main[0].paragraph[0]"></div>
            </div>
            <div v-else-if="content==1">
                content1
            </div>
            <div v-else-if="content==2">
                content2
            </div>
            <div v-else-if="content==3">
                content3
            </div>
            <div v-else-if="content==4">
                content4
            </div>
            <div v-else-if="content==5">
                content5
            </div>
        </div>
    </div>
</template>

<style scoped rel="stylesheet" type="text/css">
#layout{
    width: 100vw;
    height: 100vh;
    padding: 2.96vh;

    font: Taipei Sans TC Beta;
}
.title{
    font-style: normal;
    font-weight: bold;
    font-size: 2.47vh;
    line-height: 4.19vh;
    color: #5C5C5C;
}
.author{
    font-style: normal;
    font-weight: normal;
    font-size: 1.85vh;
    line-height: 2.47vh;
    color: #C7C7C7;
}
.font{
    font-style: normal;
    font-weight: normal;
    font-size: 1.85vh;
    line-height: 3.21vh;
    color: #5C5C5C;
}
.font_bold{
    font-style: normal;
    font-weight: bold;
    font-size: 1.85vh;
    line-height: 3.21vh;
    color: #5C5C5C;
}
.pic_box{
    display: flex;
    justify-content: center;
    padding: 2.1vh 0 2.1vh 0;
}
</style>

<script>
import Nav from '@/components/Nav.vue'

export default {
    name: 'Content',
    components: {
        Nav
    },
    data() {
        return {
            content: 0,
            main: [
                {
                    title: '什麼是心理諮商？',
                    author: '心輔組 ',
                    paragraph: [
                        '心理諮商就像一趟成長的旅程，在安全、自由與接納的空間裡，與心理師一起瞭解所遇到的困境，一起討論、釐清，並試著去處理自己的議題，為所面臨的問題找到可能的因應之道。',
                        '我們在人生的各個階段，無論是在學業、感情、生活、人際、情緒、未來方向等等，都有可能會遇到挫折與疑惑，適時的找到方法或外在資源來協助自己，能讓我們更快度過低潮，重新掌握內在的潛能、看到那個其實很有力量的自己。',
                    ]
                }
            ]
        }
    },
    methods: {

    },
    mounted() {
        this.content = this.$route.params.number;
    }
}
</script>