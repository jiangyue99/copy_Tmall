<template>
  <ul v-if="!user">
    <li>
      <div class="menu-up">
        <span>喵，欢迎来天猫</span>
      </div>
    </li>
    <li>
      <div class="menu-up">
        <a href="https://login.tmall.com/">请登录</a>
      </div>
    </li>
    <li>
      <div class="menu-up">
        <a href="https://register.tmall.com/">免费注册</a>
      </div>
    </li>
  </ul>
  <ul v-else>
    <li>
      <div class="menu-up">
        <span>Hi，</span><a href="">{{ user.id }}</a>
      </div>
    </li>
    <li>
      <div class="menu-up">
        <a href="">积分{{ user.integration }}</a>
      </div>
    </li>
    <li>
      <div class="menu-up">
        <a href="">退出</a>
      </div>
    </li>
  </ul>
  <ul class="quick-menu">
    <li>
      <div class="after-triangle menu-up">
        <a href="">我的淘宝</a>
      </div>
      <div class="menu-down">
        <a href="">已买到的宝贝</a>
        <a href="">已卖出的宝贝</a>
      </div>
    </li>
    <li>
      <div class="before-car-icon menu-up">
        <a href="">购物车</a>
      </div>
    </li>
    <li>
      <div class="after-triangle menu-up">
        <a href="">收藏夹</a>
      </div>
      <div class="menu-down">
        <a href="">收藏的宝贝</a>
        <a href="">收藏的店铺</a>
      </div>
    </li>
    <li>
      <div class="menu-up">
        <span class="separate-line"></span>
      </div>
    </li>
    <li>
      <div class="before-phone-icon menu-up">
        <a href="">手机版</a>
      </div>
      <div class="menu-down top-triangle">
        <div class="qrcode"></div>
        <b class="under"></b>
        <b class="top"></b>
      </div>
    </li>
    <li>
      <div class="menu-up">
        <a href="">淘宝网</a>
      </div>
    </li>
    <li>
      <div class="after-triangle menu-up">
        <a href="">商家支持</a>
      </div>
      <div class="menu-down">
        <div>
          <b>商家：</b>
          <ul>
            <li><a href="">商家中心</a></li>
            <li><a href="">天猫规则</a></li>
            <li><a href="">商家入驻</a></li>
            <li><a href="">运营服务</a></li>
            <li><a href="">商家品控</a></li>
            <li><a href="">商家工具</a></li>
            <li><a href="">天猫智库</a></li>
            <li><a href="">喵言喵语</a></li>
          </ul>
        </div>
        <div></div>
      </div>
    </li>
    <li>
      <div class="after-triangle before-list-icon menu-up">
        <span>网站导航</span>
      </div>
      <div class="menu-down">
      </div>
    </li>
  </ul>
</template>

<style scoped>
  ul {
    list-style-type: none;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    margin: auto 0px;
    padding: 0px;
  }

  li {
    position: relative;
  }

  span {
    display: inline;
    line-height: 20px;
  }

  .separate-line {
    height: 14px;
    vertical-align: top;
    position: absolute;
    top: 3px;
    left: 13px;
    font-size: 0;
    margin: 0px;
    border-left: 1px solid #ccc;
    }

  li div.menu-up {
    display: flex;
    padding: 0px 10px;
    font-family: "Microsoft YaHei",tahoma,arial,'Hiragino Sans GB','\5b8b\4f53',sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 12px;
    color: #999;
    margin: 0px;
  }

  li div.menu-up.after-triangle::after {
    content: '';
    position: absolute;
    display: block;
    top: 9px;
    right: 3px;
    width: 6px;
    height: 3px;
    background-image: url('/image/HeadTriangle.svg');
    background-repeat: no-repeat;
  }

  li div.menu-up.before-car-icon::before {
    content: '';
    display: block;
    margin: auto 0px auto 4px;
    width: 12px;
    height: 12px;
    background-image: url('/image/ShoppingCar.svg');
    background-repeat: no-repeat;
  }

  li div.menu-up.before-phone-icon::before {
    content: '';
    display: block;
    margin: auto 0px;
    width: 10px;
    height: 10px;
    background-image: url('/image/Phone.svg');
    background-repeat: no-repeat;
  }

  li div.menu-up.before-list-icon::before {
    content: '';
    display: block;
    margin: auto 0px auto 4px;
    width: 12px;
    height: 12px;
    background-position-y: 1px;
    background-image: url('/image/List.svg');
    background-repeat: no-repeat;
  }

  a {
    text-decoration-line: none;
    line-height: 20px;
  }

  a:visited {
    color: #999;
  }

  a:hover {
    color:#FF0036;
  }

  li div.menu-up.after-triangle a:hover {
    text-decoration-line: underline;
  }

  li div.menu-down {
    position: absolute;
    display: flex;
    flex-direction: column;
    padding: 5px 9px;
    white-space: nowrap;
    font-family: "Microsoft YaHei",tahoma,arial,'Hiragino Sans GB','\5b8b\4f53',sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    font-size: 12px;
    color: #666;
    border: 1px solid #ddd;
    border-radius: 3px;
    background-color: #fff;
    box-shadow: 0 0 2px 1px rgba(221,221,221,0.8);
  }

  div.menu-down a:visited {
    color: #666;
  }

  div.menu-down a:hover {
    color:#FF0036;
    text-decoration-line: underline;
  }

  .top-triangle {
    left: -50px;
  }

  .top-triangle b.under {
    display: block;
    position: absolute;
    top: -7px;
    left: 84px;
    height: 0px;
    width: 0px;
    border-width: 3px;
    border-style: solid;
    border-color: transparent transparent #ddd transparent;
  }

  .top-triangle b.top {
    display: block;
    position: absolute;
    top: -8px;
    left: 83px;
    height: 0px;
    width: 0px;
    border-width: 4px;
    border-style: solid;
    border-color: transparent transparent #fff transparent;
  }

  .top-triangle div {
    display: block;
    width: 175px;
    height: 210px;
    margin-bottom: 10px;
    background-image: url('/image/TmallQRcode.png'), url('/image/TmallQRcodeDescribe.jpg');
    background-repeat: no-repeat, no-repeat;
    background-position: center top, center bottom;
  }
</style>
