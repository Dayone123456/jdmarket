<template>
  <div id="find">
    <header class="top_bar">
      <a onclick="window.history.go(-1)" class="icon_back"></a>
      <h3 class="cartname">发现频道</h3>
      <a href="#" class="icon_menu"></a>
    </header>
    <ul class="md-tab_inner">
      <li  v-for="(item, index) in mainDatas" :key="index">
        <div>
          <img class="img_two" v-lazy="item.img_url[0]" alt="">
          <img  v-lazy="item.img_url[1]" alt="">
        </div>
        <span>{{item.msg}}</span>
        <div class="ic"></div>
      </li>
    </ul>
    <ul class="md_list">
      <li v-for="(item, index) in [,,,,,,,]" :key="index" >
        <div class="md_list_left">
          <div class="mll_cont">
            起球毛衣是今年的流行？！真是越来越看不懂时尚了
          </div>
          <div class="mll_def">
            <div class="mll_def_left">
               <img src="http://m.360buyimg.com/mobilecms/jfs/t2395/165/1992531123/10619/a4247e0/56e8dae2N799695e8.png.webp" alt="">
            </div>
            <span>南极星...</span>
            <span class="mll_def_right">
              15人阅读
            </span>
          </div>
        </div>
        <div class="md_list_right">
          <img src="//m.360buyimg.com/mobilecms/jfs/t18733/39/722505054/152959/f6228dfb/5aa21901Nf7cfbbf8.jpg!q70.jpg.dpg" alt="">
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data () {
    return {
      mainDatas: [{
        msg:'精选',
        img_url:[                             '//img12.360buyimg.com/jdphoto/jfs/t14824/4/1991033145/1604/f083ab0a/5a65443aN38b9804d.png.webp',
        '//img10.360buyimg.com/jdphoto/jfs/t14338/362/2005547105/687/9db36e0/5a654458N79195588.png.webp'
        ]
      }, {
        msg:'好吃的',
        img_url:[              '//img10.360buyimg.com/jdphoto/jfs/t19006/246/228142871/1773/8721cd3b/5a654489N1a3be41b.png.webp',
        '//img11.360buyimg.com/jdphoto/jfs/t16981/209/243148469/1361/c8e982af/5a65449aN1593fb13.png.webp'
        ]
      }, {
        msg:'好玩的',
        img_url:[     '//img20.360buyimg.com/jdphoto/jfs/t19012/262/233017295/892/29ab0cf3/5a6544b2N83129a6d.png.webp',
        '//img12.360buyimg.com/jdphoto/jfs/t16114/302/1791640005/552/5fae6e26/5a6544c4N72efe376.png.webp'
        ]
      }, {
        msg:'好看的',
        img_url: [        '//img10.360buyimg.com/jdphoto/jfs/t15658/245/1612107637/1443/682550aa/5a654536N8765a163.png.webp',
        '//img20.360buyimg.com/jdphoto/jfs/t15592/104/1999105092/881/e045a4f3/5a7170ebNf415f257.png.webp'
        ]
      }, {
        msg:'购物百科',
        img_url: [
        '//img10.360buyimg.com/jdphoto/jfs/t18487/363/230512497/499/3790e091/5a65454cNd14da231.png.webp',
        '//img10.360buyimg.com/jdphoto/jfs/t16378/268/1981265420/352/a8652187/5a6f1b68N095f3d2c.png.webp'
        ]
      }],
    };
  }
};
</script>
<style lang="scss" scoped>
  .top_bar {
    position: static;
  }
  img {

    max-width: 100%;
    display: block
  }
  .md-tab_inner {
    overflow: hidden;
    height: 62px;
    li {
      background-color: white;
      height: 100%;

      text-align: center;
      float: left;
      width: 20%;
      font-size: 12px;

      div {
        height: 18px;
        width: 18px;
        margin: 3px auto 5px;
        position: relative;
        .img_two {
          position: absolute;
          left: 50%;
          margin-left: -9px;
          top: 0px;
        }
      }
      .ic {
        // background: blue;
        border-left: 10px solid transparent;
        border-right: 10px solid transparent;
        border-bottom: 10px solid white;
      }
    }
    li:first-child {
      background: -webkit-linear-gradient(left, rgb(233, 59, 61), rgb(255, 149, 116));
    }
  }
  .md_list {
    background-color: rgb(243, 243, 243);
    max-width: 95%;
    margin: 10px auto;
    li {
      margin-top: 10px;
      background-color: white;
      overflow: hidden;
      height: 120px;
      .md_list_left {

        margin-top: 7px;
        margin-left: 7px;
        float: left;
        width: 60%;
        .mll_cont {
          color: #333;
          font-size: 16px;
        }
        .mll_def {
          margin-top: 40px;

          height: 33px;
          line-height: 33px;
          // overflow: hidden;
          .mll_def_left {
            float: left;
            width: 30px;
          }
          .mll_def_right {
            float: right;
            width: 60px;
          }
        }
      }
      .md_list_right {

        margin-right: 7px;
        margin-top: 7px;
        background-color: saddlebrown;
        float: right;
        width: 35%;
      }
    }
  }
</style>
