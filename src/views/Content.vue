<template>
    <div>
        <Nav showBackArrow=true showText=true navText="讀讀文章"></Nav>
        <div id="layout">
            <div v-if="content==0">
                <div class="title" v-text="main[0].title"></div>
                <div class="author" v-text="main[0].author"></div>
                <div class="pic_box"><img style="height:19.96vh" src="@/assets/anson/0610/c0p0.png"></img></div>
                <div class="font" v-text="main[0].paragraph[0]"></div>
                <br>
                <div class="font" v-text="main[0].paragraph[1]"></div>
                <br>
                <div class="font" v-text="main[0].paragraph[2]"></div>
                <br>
                <div class="font_bold" v-text="main[0].paragraph[3]"></div>
                <div class="font" v-text="main[0].paragraph[4]"></div>
                <br>
                <div class="font" v-text="main[0].paragraph[5]"></div>
                <br>
                <div class="font" v-text="main[0].paragraph[6]"></div>
                <br>
                <div class="font" v-text="main[0].paragraph[7]"></div>
            </div>
            <div v-else-if="content==1">
                <div class="title" v-text="main[1].title"></div>
                <div class="author" v-text="main[1].author"></div>
                <div class="pic_box"><img style="height:19.96vh" src="@/assets/anson/0610/c1p0.png"></img></div>
                <div class="font" v-text="main[1].paragraph[0]"></div>
                <br>
                <div class="font" v-text="main[1].paragraph[1]"></div>
                <br>
                <div class="font" v-text="main[1].paragraph[2]"></div>
                <br>
                <div class="font" v-text="main[1].paragraph[3]"></div>
                <br>
                <div class="font" v-text="main[1].paragraph[4]"></div>
                <br>
                <div class="font" v-text="main[1].paragraph[5]"></div>
                <div class="pic_box"><img style="height:19.96vh" src="@/assets/anson/0610/c1p1.png"></img></div>
                <div class="font" v-text="main[1].paragraph[6]"></div>
                <br>
                <div class="font" v-text="main[1].paragraph[7]"></div>
                <div class="font" v-text="main[1].paragraph[8]"></div>
                <div class="font" v-text="main[1].paragraph[9]"></div>
                <div class="font" v-text="main[1].paragraph[10]"></div>
                <div class="font" v-text="main[1].paragraph[11]"></div>
                <br>
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
            <br>
        </div>
        <Footer showResouce=true />
    </div>
</template>

<style scoped rel="stylesheet" type="text/css">
#layout{
    width: 100vw;
    padding: 2.96vh;

}
.title{
    font: Taipei Sans TC Beta;
    font-style: normal;
    font-weight: bold;
    font-size: 2.47vh;
    line-height: 4.19vh;
    color: #5C5C5C;
}
.author{
    font: Taipei Sans TC Beta;
    font-style: normal;
    font-weight: normal;
    font-size: 1.85vh;
    line-height: 2.47vh;
    color: #C7C7C7;
}
.font{
    font: Taipei Sans TC Beta;
    font-style: normal;
    font-weight: normal;
    font-size: 1.85vh;
    line-height: 3.21vh;
    color: #5C5C5C;
}
.font_bold{
    font: Taipei Sans TC Beta;
    font-style: normal;
    font-weight: 900;
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
import Footer from '@/components/Footer.vue'
export default {
    name: 'Content',
    components: {
        Nav,
        Footer
    },
    data() {
        return {
            content: 0,
            main: [
                {
                    title: '什麼是心理諮商？',
                    author: '心輔組 ',
                    paragraph: [
                        '心理諮商就像一趟成長的旅程，在安全、自由與接納的空間裡，與心理師一起瞭解所遇到的困境，一起討論、釐清，並試著去處理自己的議題，為所面臨的問題找到可能的因應之道。'
                        ,'我們在人生的各個階段，無論是在學業、感情、生活、人際、情緒、未來方向等等，都有可能會遇到挫折與疑惑，適時的找到方法或外在資源來協助自己，能讓我們更快度過低潮，重新掌握內在的潛能、看到那個其實很有力量的自己。'
                        ,'心理諮商也許不能將我們所遭遇的問題直接去除，但能讓我們擁有更多能量與策略去面對挑戰及有所成長，用更好的自己去迎接未來。'
                        ,'除了各別心理諮商外，還有「團體心理諮商」'
                        ,'團體心理諮商是藉由領導者的帶領，讓參加團體的成員彼此互相交換與分享想法、感覺來瞭解自我與瞭解他人。'
                        ,'團體通常每週進行一次，共進行六至十週，視不同主題安排而定，目的都是幫助成員更深入探索自己的內心世界。'
                        ,'團體諮商與各別諮商不同之處在於可以同時與許多人互動，從中也能培養聆聽、同理、表達等人際互動技巧，且透過大家的分享獲得普同感，讓自己在成長的路上不孤單。'
                        ,'心輔組每學期也都會舉辦許多不同主題的團體，歡迎大家視自己的需求參加！'
                    ]
                },
                {
                    title: '良好的睡眠，從白天開始',
                    author: '心輔組 張文耀心理師',
                    paragraph: [
                        '睡眠不是從躺上床的那一刻開始嗎？如果你真的這麼想，那你就是把睡眠這件事看得太容易、太單純了。對於沒有睡眠困擾的人來說，有沒有這種看法可能沒什麼差別，但對於正飽嚐失眠之苦的人來說，這樣的看法不但無助於改變現況，更會讓良好的睡眠猶如水中月一般，看得到卻碰觸不著。'
                        ,'哲人尼采說過：「睡眠這件事並不渺小，為了它你需要維持整天的清醒」，可見夜裡的睡眠與白天的所作所為有極大的關係。他還說「你必須在白天找到十個真理，否則將在夜裡探索真理」。換句話說，要跨到睡眠狀態的容易程度，有很大部分取決於你醒著的時間。你要能對一整天的努力感到滿意，才能成功地結束這一天，到夜深人靜的時候，你才有辦法讓心靈安歇下來，以便能進入睡眠。'
                        ,'白天的哪些事會跟睡眠息息相關呢？第一個就是清醒的時間長度。睡眠就跟吃飯喝水等等生理功能一樣，缺乏了就要補充，缺乏越久，就越渴望獲得滿足，亦即，醒得越久就越想睡。所以白天多從事活動，避免小睡時間過長，都可以讓我們在睡覺前的睡眠驅力達到高峰，等到躺床的那一刻，才會由衷地湧現「睡覺真好」的感覺。'
                        ,'第二件事是擔憂。雖然這跟天生的個性有關，但也可以透過後天的練習進行調整。有的人在白天擔憂一堆事，整天都持續在情緒高亢的狀態，但了晚上繼續擔憂。擔憂會激發清醒系統，即使身體再累，睡眠驅力再強，擔憂的心總是會影響你的睡眠。因此，平時應盡量把事情處理好，但了晚上才不會又記掛這些事。即使事情沒處理完，也可以先用筆寫下來，再把你設想的解決方案也列下來，明天醒來繼續處理，這些事就可以暫時放下了。'
                        ,'第三是你對睡眠的一些不正確的觀念，這些不正確的觀念就可能在你睡不好的時候影響你，讓你嚐到持續失眠的滋味。那我們還會有哪些錯誤觀念呢？以下整理一些常見的睡眠迷思。這些觀念之所以稱為迷思，是因為它看起來好像是正確的，但是實際上並非如此。例如：每天一定要睡8小時才「正常」嗎？不一定！每個人需要的睡眠長度不同。睡到自然醒最好？這要看自然醒是怎麼醒，睡太久反而干擾生理時鐘的規律。睡不著時，躺著休息也好？雖然很多人會勸睡不好的人這麼做，但躺越久會越睡不著，即使睡著也只是淺眠！睡不好一定會影響隔天的工作狀況嗎？雖然隔天精神會受影響，但不見得會影響工作表現，過度擔心睡不好反而影響更大！假日補眠是減少睡眠債的好方法嗎？適度補眠（晚1小時起床）可減少睡眠債，但過度補眠卻會干擾生理時鐘與作息！因為睡不好，所以應該盡量減少活動的參與來補眠嗎？不可，活動太少會降低睡眠驅力，不利於晚上的睡眠。'
                        ,'此外，即使我們都不希望睡眠問題越拖越久，但是我們在白天所做的一些補償失眠的努力，可能會讓失眠持續下去。有哪些常見的錯誤補償方式呢？在經歷了一夜或數夜的睡眠不足，很自然的，我們會想賴床、增加白天小睡的時間，或是飲用含咖啡因的飲料提神。這些方式雖然可以暫時提振精神，但是卻也破壞了睡眠驅力、刺激著清醒系統持續運作，這些影響如果持續到晚上，就會影響晚上的睡眠，造成隔天再一次的睡眠問題。'
                        ,'因此，為了晚上能好好睡一覺，增加一夜好眠的機會，我們應該要體認睡眠的重要性，不該任意改變作息時間，平時的生活也應遵循健康的生活方式，規律運動、注意健康的飲食，凡此都可以讓生理時鐘規律化。睡覺時也應保持良好的睡眠習慣，除了睡覺和性行為以外，不要在床上做其他事，夜裡睡不著應離開床，等到想睡時再躺床（刺激控制法）。此外，創造最佳的睡眠環境，降低噪音、光線的影響，對睡眠也有幫助。最後則是要留意破壞睡眠的因素，例如咖啡因、菸酒、睡前水喝太多或太少、過飽或過飢等。'
                        ,'參考書目：'
                        ,'1.李宛蓉譯，民96。哈佛醫生的優質睡眠全書。商周出版。'
                        ,'2.周舒翎、楊建銘譯，民99。不再失眠。書泉出版。'
                        ,'3.周舒翎著，民101。為什麼就是睡不著。大塊文化出版。'
                        ,'4.楊建銘著，民99。失眠可以自療。時報出版。'
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