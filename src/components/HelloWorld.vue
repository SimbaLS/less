<template>
  <div id="app">
    <section class="head">
      <div class="box">
        <img src="/src/assets/melon.png" alt="">
      </div>
      <div class="name">
        <span>哈哈哈哈</span>
        <img src="/src/assets/v_club.png" alt="">
      </div>
      <div class="head-r">
        <p class="integrity">诚信度：12</p>
        <p class="dark">已通过平台企业认证</p>
      </div>
    </section>

    <section class="score">
      <div>
        <p class="score-title">赞助承诺兑现</p>
        <ul class="score-c">
          <li>
            <img src="/src/assets/star_y.png" alt="">
          </li>
          <li>
            <img src="/src/assets/star_d.png" alt="">
          </li>
        </ul>
        <p class="score-r">
          <span>1分</span>
          <span>非常不好</span>
        </p>
      </div>
      <div>
        <p class="score-title">商家沟通状况</p>
        <ul class="score-c">
          <li>
            <img src="star_y.png" alt="">
          </li>
          <li>
            <img src="star_d.png" alt="">
          </li>
        </ul>
        <p class="score-r">
          <span>12分</span>
          <span>非常好</span>
        </p>
      </div>
    </section>
    <section class="total">
      <p>累计赞助<span class="red">23</span>次</p>
      <p>累计<span class="red">32</span>元赞助金</p>
      <p>累计<span class="red">23</span>次物资赞助</p>
      <p>本月受罚(次):<span>1</span></p>
      <p>近900天受罚(次):<span>-</span></p>
      <p>全部受罚(次):<span>0</span></p>
    </section>
    <section class="information">
      <div class="part">
        <p class="title">企业性质：</p>
        <p class="con">国企</p>
      </div>
      <div class="part">
        <p class="title">企业规模：</p>
        <p class="con">1-12人</p>
      </div>
      <div class="synopsis">
        <p class="title">企业简介：</p>
        <p class="dark">企业未添加简介企业未添加简介企业未添加简介企业未添加简介企业未添加简介企业未添加简介企业未添加简介企业未添加简介企业未添加简介企业未添加简介企业未添加简介</p>
      </div>
      <div class="part disFlex">
        <p class="title">联系人：</p>
        <p class="dark">sususs</p>
      </div>
      <div class="part">
        <p class="title">联系电话：</p>
        <p class="con">13300000000</p>
      </div>
      <div class="part">
        <p class="title">平台电话：</p>
        <p class="con">微信同号</p>
      </div>
    </section>
    <p class="dark">确认合作后可查看联系电话，合作前的沟通可联系平台，平台对接更安全</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less" scoped>
  *{
    margin: 0;
    padding: 0;
  }
  li{
    list-style: none;
  }
  @color:#ffcf00 #E33F3F #999999 #333;
  @padding: 30px;
  @src:'/img';
  .center{
    margin: 0 auto;
  }
  .line1-4 {
    line-height: 1.4;
  }
  .disFlex{
    display: -webkit-flex;
    display: flex;
    &>* {
      flex: 0 0 auto;
    }
  }
  .fSize(@param) {
    font-size:@param ;
  }
  .font-normal(@color:#333333;@weight:400){
    color: @color;
    font-weight: @weight;
  }
  .fs {
    font-size: 12px!important;

    @media (max-width: 320px) {
      .fSize(10px) !important;
    }
    @media (min-width: 321px) and (max-width: 360px) {
      .fSize(11px) !important;
    }
  }

  .dark{
    .fSize(1em);
    @val: extract(@color, 3);
    .font-normal(@val);
  }
  .align-center{
    align-items: center;
  }
  .box {
    position: relative;
    overflow: hidden;
    &:before{
      content: "";
      display: block;
      padding-top: 100%
    }
    img{
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
    }
  }
  body{
    .center();
  }

  #app {
    padding: @padding;
    .center();
  }
  .head{
    .disFlex();
    .align-center();
    .box{
      width:1.2rem;
      max-width: 45px;
      border-radius:4px;
      margin-right: 0.267rem;
    }
    .name{
      max-width: 54%;
      margin-right: auto;
      &>*{
        display: inline;
        vertical-align: middle;
      }
      span{
        .fSize(1.25em);
        line-height: 1.2;
        .font-normal(extract(@color, 3));
      }
      img{
        width:0.427rem;
        max-width: 16px;
      }
    }
    .head-r{
      margin-left: 5px;
      .integrity{
        width: 2.427rem;
        max-width: 91px;
        margin-bottom: 2px;
        .fSize(1.16em);
        @val:extract(@color, 1);
        .font-normal(@val,500);
        background:rgba(255,249,223,1);
        border-radius:4px;
        padding: 4px 0 ;
        text-align: center;
        margin-left: auto;
      }
    }
  }

  .score{
    & >*{
      margin-top: 0.4rem;
      .disFlex();
      .align-center();
    }
    .score-title{
      .fSize(1.16em);
      .font-normal();
      .line1-4();
    }
    /*扩展*/
    .score-c:extend(.disFlex){
      .align-center();
      li>img{
        width: 0.533rem;
        max-width: 20px;
        margin-left: 0.267rem;
      }
    }
    .score-r:extend(.dark){
      & > span:first-child{
        margin: 0 0.213rem 0 0.293rem;
      }
    }
  }
  .total{
    .fSize(1.16em);
    .font-normal();
    .line1-4();
    p{
      margin-top:0.267rem;
    }
    .red{
      .font-normal(#E33F3F);
      .fSize(1.14em);
    }
    label:not(:last-child){
      margin-right: 0.267rem;
    }
  }
  .information{
    margin-bottom: 6px;
    .part:extend(.disFlex),.synopsis{
      .line1-4();
      margin-top: 0.24rem;
      .align-center();
    }
    .title{
      .fSize(1.25em);
      .font-normal(@weight:bolder);
      font-weight:bolder;
      @val:extract(@color, 4);
      color:@val;
    }
    .con{
      .fSize(1.16em);
      .font-normal();
    }
    .synopsis .dark{
      margin-top: 4px;
    }
  }
  /*test*/

  #bundle() {
    .button {
      display: block;
      border: 1px solid black;
      background-color: grey;
      &:hover {
        background-color: white;
      }
    }
    .tab { color:red;}
    .citation {
      .fSize(20px);
    }
  }

</style>
