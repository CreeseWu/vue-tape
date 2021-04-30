<template>


  <div style="width:1rem;display:none" hidden=""></div>
  <div class="bg_box" id="bg" style="background-color:rgb(188,240,230)"></div>


  <div id="questionBox">
    <div class="box-content">


      <div @click="askQuestion" class="quiz" style="height:6rem">
        <div class="cardbg" style="opacity:0.75"></div>
        <pre class="introduction" style="color:rgb(0,0,0)">征集诸位爱卿的问题</pre>
        <p class="quiz-tips" style="color:rgb(193,193,193)">点击此处向我匿名提问</p></div>


    </div>
    <div class="card-box">
      <div data-v-cd12ea="">
        <div data-v-cd12ea="" class="box_tit"><img data-v-cd12ea=""
                                                   src="data:image/jpeg;base64,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"
                                                   alt="">
          <h3 data-v-cd12ea="">小吴&NoBreak;wu的其他回答（{{ questionList.length == 0 ? "还在加载中" : questionList.length }}）</h3>
        </div>
        <div @click="visitQuestion(i.visitCode)" v-for="(i,k) in questionList" :key="k" data-v-cd12ea=""
             class="answer_card bg_white">
          <p data-v-cd12ea="" class="time">{{ i.createdAt.split(' ')[0] }}</p>
          <div data-v-cd12ea="" class="answer_title">{{ i.title }}</div>


          <img data-v-cd12ea=""
               src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB3aWR0aD0iN3B4IiBoZWlnaHQ9IjEycHgiIHZpZXdCb3g9IjAgMCA3IDEyIiB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiPgogICAgPCEtLSBHZW5lcmF0b3I6IFNrZXRjaCA1Ni4yICg4MTY3MikgLSBodHRwczovL3NrZXRjaC5jb20gLS0+CiAgICA8dGl0bGU+57yW57uEPC90aXRsZT4KICAgIDxkZXNjPkNyZWF0ZWQgd2l0aCBTa2V0Y2guPC9kZXNjPgogICAgPGcgaWQ9Img15o+Q6Zeu566xIiBzdHJva2U9Im5vbmUiIHN0cm9rZS13aWR0aD0iMSIgZmlsbD0ibm9uZSIgZmlsbC1ydWxlPSJldmVub2RkIiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiPgogICAgICAgIDxnIGlkPSIxLjMt5o+Q5Lqk5ZCO6aG16Z2iLeWMv+WQjeaPkOmXriIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoLTMzMS4wMDAwMDAsIC0xMzM3LjAwMDAwMCkiIHN0cm9rZT0iIzMzMzUzOCIgc3Ryb2tlLXdpZHRoPSIyIj4KICAgICAgICAgICAgPGcgaWQ9Iue8lue7hC0yNCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTkuMDAwMDAwLCAxMjAyLjAwMDAwMCkiPgogICAgICAgICAgICAgICAgPGcgaWQ9Iue8lue7hCIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMzE1LjUwMDAwMCwgMTQxLjAwMDAwMCkgcm90YXRlKC0xODAuMDAwMDAwKSB0cmFuc2xhdGUoLTMxNS41MDAwMDAsIC0xNDEuMDAwMDAwKSB0cmFuc2xhdGUoMzEzLjAwMDAwMCwgMTM2LjAwMDAwMCkiPgogICAgICAgICAgICAgICAgICAgIDxwYXRoIGQ9Ik00LjcyMjIyMjIyLDAuNDQ3Nzc3Nzc4IEwwLDUuMTciIGlkPSLnm7Tnur8tMTUiPjwvcGF0aD4KICAgICAgICAgICAgICAgICAgICA8cGF0aCBkPSJNNC43MjIyMjIyMiw5Ljg5MjIyMjIyIEwwLDUuMTciIGlkPSLnm7Tnur8tMTUiPjwvcGF0aD4KICAgICAgICAgICAgICAgIDwvZz4KICAgICAgICAgICAgPC9nPgogICAgICAgIDwvZz4KICAgIDwvZz4KPC9zdmc+"
               alt="" class="answer_btn">

        </div>
      </div>
    </div>
  </div>


</template>

<script>
import axios from 'axios';

const api = 'https://apiv4.tapechat.net/unuser/getQuestionFromUser/IKM4IF45?pageSize=2000&lastTimeStamp=1619761358528'


export default {
  data() {
    return {
      questionList: []
    }

  }
  ,
  methods: {

    visitQuestion(qid) {
      const url = 'https://www.tapechat.net/answeredDetail.html?dynamicId=' + qid
      window.location.href = url
    },
    askQuestion() {
      window.location.href = 'https://www.tapechat.net/u/kriswoo/IKM4IF45'
    }
  },
  mounted: function () {

    axios.get(api).then(
        (response) => {
          console.log(response.data.content.data)
          this.questionList = response.data.content.data
        }
    );
  }

}


</script>

<style>.box_tit[data-v-cd12ea] {
  margin: 0 auto;
  display: flex;
  align-items: center
}

.box_tit > img[data-v-cd12ea] {
  width: 1.33333333rem;
  height: 1.33333333rem;
  border-radius: 50%;
  margin-right: .26666667rem
}

.box_tit > h3[data-v-cd12ea] {
  font-size: .37333333rem;
  font-weight: 600;
  color: #000;
  line-height: .53333333rem
}

.answer_card[data-v-cd12ea] {
  padding: .34666667rem .48rem;
  height: 3.89333333rem;
  box-sizing: border-box;
  border-radius: .21333333rem;
  margin: .26666667rem auto 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between
}

.answer_title[data-v-cd12ea] {
  font-size: .37333333rem;
  color: #000;
  text-overflow: ellipsis;
  overflow: hidden;
  display: -webkit-box;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  word-break: break-all
}

.time[data-v-cd12ea] {
  font-size: .24rem;
  font-weight: 600;
  color: #c1c1c1
}

.answer_btn[data-v-cd12ea] {
  width: .13333333rem;
  height: .26666667rem;
  margin-left: auto
}

.ques_download[data-v-cd12ea] {
  width: 8.13333333rem;
  height: 1.06666667rem;
  display: block;
  margin: .8rem auto 0;
  border-radius: .10666667rem;
  font-size: .37333333rem;
  font-weight: 600;
  color: #fff;
  line-height: 1.06666667rem;
  text-align: center
}

html {
  color: #303030;
  background: #fff
}

body {
  font-family: PingFang SC, miui, "system-ui", -apple-system, BlinkMacSystemFont, segoe ui, Roboto, Helvetica, Arial, sans-serif, apple color emoji, segoe ui emoji, segoe ui symbol
}

body, div, h3, p, pre {
  padding: 0;
  margin: 0
}

img {
  border: 0
}

.bg_white {
  background-color: #fff
}

.btn_blue {
  background-color: #56bc9f
}

body, html {
  height: 100%;
  margin: 0;
  background-color: #fff
}

h3, p {
  margin: 0
}

@media screen and (min-width: 769px) {
  #questionBox, body {
    max-width: 750px;
    margin: 0 auto
  }

  html {
    font-size: 40px !important
  }

  .jump_btn {
    max-width: 750px
  }

  .bg_box, .jump_btn {
    left: 50% !important;
    transform: translate(-50%)
  }

  .bg_box {
    width: 750px !important
  }
}

body {
  height: 100%
}

#questionBox {
  position: relative;
  padding: 0 .96rem 1.86666667rem
}

#questionBox .jump_btn {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 1.28rem;
  background: #56bc9f;
  font-size: .48rem;
  font-weight: 600;
  color: #fff;
  line-height: 1.28rem;
  text-align: center;
  z-index: 9999
}

#questionBox .card-box {
  padding-top: 24vh
}

.box-content {
  padding: 23vh 0 0
}

.quiz {
  box-sizing: border-box;
  transition: all .3s
}

.quiz {
  position: relative;
  z-index: 99
}

.quiz .cardbg {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  width: 100%;
  height: 100%;
  background-size: 100% 100%
}

.quiz .introduction {
  font-size: .42666667rem;
  padding: 1.6rem .85333333rem 0;
  line-height: .58666667rem;
  text-align: center;
  font-weight: 600;
  white-space: pre-wrap;
  white-space: -moz-pre-wrap;
  white-space: -o-pre-wrap;
  word-wrap: break-word
}

.quiz .quiz-tips {
  margin-top: 1.12rem;
  font-size: .32rem;
  font-weight: 600;
  line-height: .58666667rem;
  text-align: center
}

.tost {
  text-align: center
}

.tost {
  position: fixed;
  z-index: 9999;
  left: 50%;
  top: 50%;
  width: 6.66666667rem;
  padding: .13333333rem .26666667rem;
  -webkit-transform: translate(-50%, -50%);
  -moz-transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  -o-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
  line-height: .61333333rem;
  border-radius: .24rem;
  color: #fff;
  background: rgba(0, 0, 0, .8);
  font-size: .48rem
}

.bg_box {
  width: 100%;
  height: 100%;
  position: fixed;
  top: 0;
  left: 0;
  background-position: 50%;
  background-size: cover;
  background-repeat: no-repeat
}</style>