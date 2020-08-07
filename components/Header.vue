
<template>
  <header class="has-shadow headroom headroom--not-bottom headroom--pinned headroom--top">
    <div class="inner wide vertical">
      <div class="justify">
        <div class="left-side">
          <div id="logo">
            <a href="/">
              <img src="/images/logo.png" width="126" height="48" alt />
            </a>
          </div>
          <a v-b-toggle.sidebar-backdrop class="menu-mobile"></a>
          <b-sidebar id="sidebar-backdrop" backdrop shadow>
            <div class="py-5">
              <nuxt-link to="/kek" style="font-size: 1.5em; color: #08c0de">
                <div class="px-5 pt-3 pb-3" style="border-top: 1px solid #ccc">Врачи</div>
              </nuxt-link>
              <nuxt-link to="/" style="font-size: 1.5em; color: #08c0de">
                <div class="px-5 pt-3 pb-3" style="border-top: 1px solid #ccc; border-bottom: 1px solid #ccc">О сервисе</div>
              </nuxt-link>
            </div>
          </b-sidebar>
          <ul class="top-menu">
            <li class="active">
              <a href="/doctors/">Врачи</a>
            </li>

            <li>
              <a href="/about/">О сервисе</a>
            </li>
          </ul>
        </div>
        <div class="block-header">
          <div class="support">
            <div class="social-menu">
              <span >Техническая поддержка</span>
              <a href="tel:8 800 333 28 00" style="width: 100%;text-align:center" class="tel">7 908 035 14 53</a>
              <div class="all-support">
                <p>Другие способы связи:</p>
                <div class="social">
                  <div class="teleg">
                    <a href="https://t.me/online_doctor_bot" target="_blank"></a>
                  </div>
                  <div class="fb">
                    <a href="https://www.facebook.com/999476266806076" target="_blank"></a>
                  </div>
                  <div class="mail">
                    <a href="mailto:help@onlinedoctor.ru" target="_blank"></a>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div id="login-form">
            <a class="login login-init" data-redirect="/">Войти</a>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style>
@font-face {
  font-family: 'CirceRounded';
  src: url('~static/fonts/CirceRounded-Regular.woff2') format('woff2'),
    url('~static/fonts/CirceRounded-Regular.woff') format('woff'),
    url('~static/fonts/CirceRounded-Regular.ttf') format('truetype');
}
body {
  width: 100%;
  height: 100%;
  min-height: 100%;
  padding-top: 80px !important;
  color: #000000;
  font-family: 'CirceRounded';
  font-weight: bold;
}
header {
  background: #ffffff;
  width: 100%;
  min-width: 960px;
  font-weight: normal;
  text-align: center;
  position: fixed;
  top: 0;
  z-index: 1010;
  -webkit-transition: box-shadow 0.1s ease-out 0s;
  -webkit-transition: -webkit-box-shadow 0.1s ease-out 0s;
  transition: -webkit-box-shadow 0.1s ease-out 0s;
  transition: box-shadow 0.1s ease-out 0s;
  transition: box-shadow 0.1s ease-out 0s, -webkit-box-shadow 0.1s ease-out 0s;
}
header.has-shadow {
  -webkit-box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.1);
  box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.1);
}
.inner.wide {
  width: 1184px;
  min-width: 320px;
  padding-left: 0;
  padding-right: 0;
}
.inner {
  width: 1164px;
  min-width: 320px;
  margin: 0 auto;
  padding-left: 0;
  padding-right: 0;
}
header .content,
header .inner {
  height: 80px;
}
header .content,
header .inner {
  height: 80px;
}
body .vertical::before {
  content: '';
  display: inline-block;
  vertical-align: middle;
  height: 100%;
}
body .vertical > * {
  display: inline-block;
  vertical-align: middle;
}
body .justify {
  width: 100%;
  text-align: justify;
  text-justify: inter-word;
}
header .content .left-side,
header .inner .left-side {
  float: left;
  padding-top: 4px;
}
.justify > * {
  display: inline-block;
  vertical-align: middle;
}
header .content .left-side #logo,
header .inner .left-side #logo {
  display: inline-block;
  margin-right: 30px;
  cursor: pointer;
}
img {
  vertical-align: middle;
}
img {
  border: 0;
}
header .content .left-side #logo > a,
header .inner .left-side #logo > a {
  display: block;
  width: 100%;
  height: 100%;
}
a {
  text-decoration: none;
  font-size: inherit;
  font-weight: inherit;
  outline: none;
}
body.pacient a {
  color: #08c0de;
}
header .content .left-side .menu-mobile,
header .inner .left-side .menu-mobile {
  width: 24px;
  height: 24px;
  background: url(/images/menu.svg);
  display: none;
}
header .content .left-side .top-menu,
header .inner .left-side .top-menu {
  list-style: none;
  font-size: 18px;
}
header .content .left-side > div,
header .inner .left-side > div,
header .content .left-side > ul,
header .inner .left-side > ul {
  display: inline-block;
  vertical-align: middle;
}
ul {
  margin: 0;
  padding: 0;
  list-style: none;
}
.top-menu > li.active,
header .content .left-side .top-menu > li:hover,
header .inner .left-side .top-menu > li:hover {
  color: #00aabe;
}
a:hover {
  text-decoration: none !important;
}
.top-menu > li:first-child {
  padding-top: 0;
}
.top-menu > li {
  display: inline-block;
  vertical-align: middle;
  margin-right: 20px;
  color: #333333;
  -webkit-transition: color 0.2s ease-in-out 0s;
  transition: color 0.2s ease-in-out 0s;
}
header .content .left-side .top-menu > li a,
header .inner .left-side .top-menu > li a {
  font-weight: normal;
  color: inherit;
}

header .block-header {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: horizontal;
  -webkit-box-direction: normal;
  -ms-flex-direction: row;
  flex-direction: row;
  -webkit-box-pack: end;
  -ms-flex-pack: end;
  justify-content: flex-end;
  -webkit-box-align: center;
  -ms-flex-align: center;
  align-items: center;
  -ms-flex-wrap: wrap;
  flex-wrap: wrap;
}

.support {
  margin-right: 40px;
  position: relative;
}
.support .social-menu {
  cursor: pointer;
  padding: 5px 10px 8px;
  overflow: hidden;
}
.support .social-menu span {
  display: block;
  line-height: 1.1;
  font-size: 16px;
  font-family: 'CirceRounded';
  font-weight: normal;
  color: #b7b9bb;
  position: relative;
  z-index: 10;
}
.support .social-menu .tel {
  line-height: 1.1;
  font-size: 24px;
  font-family: 'CirceRounded';
  color: #00aabe;
  position: relative;
  z-index: 10;
  margin-bottom: 0;
  border-bottom: 1px dashed #00aabe;
  display: inline-block;
  font-weight: bold;
}
.support .all-support {
  opacity: 0;
  position: absolute;
  top: 0;
  padding: 76px 24px 26px;
  width: 216px;
  left: 50%;
  margin: -20px 0 0 -108px;
  text-align: center;
  visibility: hidden;
  background: white;
  -webkit-box-shadow: 0px 2px 7px rgba(0, 0, 0, 0.15);
  box-shadow: 0px 2px 7px rgba(0, 0, 0, 0.15);
  border-radius: 8px;
  -webkit-transition: opacity 0.5s ease-out;
  transition: opacity 0.5s ease-out;
}
.support .all-support p {
  padding: 16px 0 8px;
  border-top: 1px solid #ededed;
  font-size: 16px;
  margin-bottom: 0;
}
header #login-form {
  font-size: 18px;
}
header #login-form .login {
  display: inline-block;
  vertical-align: middle;
  color: inherit;
  cursor: pointer;
  position: relative;
  font-weight: normal;
  font-size: 18px;
  line-height: 20px;
}
header #login-form .login:before {
  content: '';
  display: inline-block;
  vertical-align: middle;
  background: url(/images/enter_icon.svg) no-repeat;
  background-size: contain;
  width: 24px;
  height: 24px;
  margin-right: 4px;
  margin-top: -5px;
}

@media only screen and (max-width: 1204px) {
  header {
    min-width: 320px;
    width: 100%;
  }
  .inner.wide {
    width: 100%;
    padding-left: 45px;
    padding-right: 45px;
  }
}

@media only screen and (max-width: 1023px) {
  header .content .left-side .menu-mobile,
  header .inner .left-side .menu-mobile {
    display: block;
    margin-right: 30px;
  }
  #container {
    margin: 0 auto;
  }
  .inner.wide {
    width: 100%;
    padding-left: 32px;
    padding-right: 32px;
  }
  header .content .left-side,
  header .inner .left-side {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    -ms-flex-direction: row;
    flex-direction: row;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center;
  }
  header .content .left-side .top-menu,
  header .inner .left-side .top-menu {
    display: none;
  }
  header .content .left-side #logo,
  header .inner .left-side #logo {
    -webkit-box-ordinal-group: 3;
    -ms-flex-order: 2;
    order: 2;
  }
  header .content .left-side .menu-mobile,
  header .inner .left-side .menu-mobile {
    display: block;
    margin-right: 30px;
  }
}

@media only screen and (max-width: 765px){
    #container {
        margin: 0 auto;
    }
    header .content .left-side, header .inner .left-side {
        width: 90%;
        padding-top: 0;
    }
    header .content .left-side, header .inner .left-side {
        display: -webkit-box;
        display: -ms-flexbox;
        display: flex;
        -webkit-box-orient: horizontal;
        -webkit-box-direction: normal;
        -ms-flex-direction: row;
        flex-direction: row;
        -webkit-box-align: center;
        -ms-flex-align: center;
        align-items: center;
    }
    header .content .left-side #logo, header .inner .left-side #logo {
        text-align: center;
        -webkit-box-flex: 1;
        -ms-flex: 1;
        flex: 1;
        width: 90%;
    }
    header .content .left-side #logo, header .inner .left-side #logo {
        -webkit-box-ordinal-group: 3;
        -ms-flex-order: 2;
        order: 2;
    }
    header .block-header .support {
        margin-right: 0;
    }
    header #login-form {
        display: none;
    }
    header .block-header .support a.tel {
        text-indent: -9999px;
        width: 24px;
        height: 24px;
        margin-top: 6px;
        border-bottom: 0;
        background: url(/images/Phone.svg) no-repeat;
    }
    header .block-header .support span {
        display: none;
    }
}

</style>
