<template>
<div>
  <div id="dashboard">
    <div class="dashboard_banner">
      <div class="inner inner-center">
        
        <div class="left-block">
          <h2 class="title indent-4">Консультация дежурного врача</h2>

          <div class="description">
            Опытный дежурный врач свяжется с вами в течение
            <strong>3 минут</strong>, проведет осмотр по видеосвязи, задаст вопросы и даст рекомендации
          </div>
        </div>
        <div class="doctors-wrapper justify">
          <div class="doctor-1">
            <div class="price">800 ₽</div>
            <h3 class="name">Терапевт</h3>
            <div class="about">Врач общего профиля для взрослых людей</div>
            <b-button class="dash-btn" variant="info">Начать консультацию</b-button>
          </div>
          <div class="doctor-2">
            <div class="price">800 ₽</div>
            <h3 class="name">Педиатр</h3>
            <div class="about">Детский врач для пациентов, не достигших 18 лет</div>
            <b-button class="dash-btn" variant="danger">Начать консультацию</b-button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <SearchDoctor  />
  </div>
</template>

<script>
export default {}
</script>

<style>
  .dashboard_banner {
    min-width: 1204px;
    padding: 48px 0 48px;
    background: #60c1ce;
    background-size: cover;
    background-position: bottom;
  }
  .dashboard_banner .inner.inner-centerd {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: horizontal;
    -webkit-box-direction: normal;
    -ms-flex-direction: row;
    flex-direction: row;
    -ms-flex-pack: distribute;
    justify-content: space-around;
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
    -webkit-box-align: center;
    -ms-flex-align: center;
    align-items: center !important;
  }
  .dashboard_banner .inner.inner-center, .dashboard_banner .inner.inner-center {
      display: -webkit-box;
      display: -ms-flexbox;
      display: flex;
      -webkit-box-orient: horizontal;
      -webkit-box-direction: normal;
      -ms-flex-direction: row;
      flex-direction: row;
      -ms-flex-pack: distribute;
      justify-content: space-around;
      -ms-flex-wrap: wrap;
      flex-wrap: wrap;
      -webkit-box-align: center;
      -ms-flex-align: center;
      align-items: center !important;
  }
  .dashboard_banner .left-block {
    width: 350px !important;
  }
  .dashboard_banner h2.title {
    font-weight: bold;
    font-size: 32px;
    line-height: 34px;
    color: white;
    margin: 0;
    padding: 0 0 24px;
  }
  .dashboard_banner .description {
    font-weight: normal;
    font-size: 18px;
    line-height: 26px;
    color: white;
  }
  .dashboard_banner .doctors-wrapper {
    width: auto;
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
    -ms-flex-wrap: wrap;
    flex-wrap: wrap;
  }
  .dashboard_banner .doctors-wrapper > div.doctor-1,
  .dashboard_banner .doctors-wrapper > div.doctor-2 {
    display: -webkit-box;
    display: -ms-flexbox;
    display: flex;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    -ms-flex-direction: column;
    flex-direction: column;
    -webkit-box-pack: start;
    -ms-flex-pack: start;
    justify-content: flex-start;
  }
  .dashboard_banner .doctor-2 .price, .dashboard_banner .doctor-2 .price-container {
      color: #f0505a !important;
  }
  #dashboard  .dashboard_banner .doctors-wrapper .price:before {
      content: "";
      position: absolute;
      width: 48px;
      height: 48px;
      background: url(/images/terapevt.png) no-repeat;
      left: 0;
      top: 0;
  }
  #dashboard  .dashboard_banner .doctor-2 .price:before, #dashboard  .dashboard_banner .doctor-2 .price-container:before {
      background: url(/images/pediatr.png) no-repeat;
  }
  .dashboard_banner .doctor-2 {
      margin-left: 50px;
  }
  .dashboard_banner .doctors-wrapper > div {
    width: 264px;
    border-radius: 15px 15px 15px 15px;
    vertical-align: top;
    text-align: left;
    padding: 24px 24px 26px;
    -webkit-box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.15);
    box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.15);
    background: white;
  }
  .dashboard_banner .doctors-wrapper .price,
  .dashboard_banner .doctors-wrapper .price-container {
    width: 100%;
    text-align: right;
    font-weight: normal;
    position: relative;
    font-size: 28px;
    line-height: 34px;
    height: 48px;
    margin-bottom: 24px;
    padding-left: 48px;
    color: #00aabe;
  }
  .dashboard_banner .doctors-wrapper > div.doctor-1 h3.name,
  .dashboard_banner .doctors-wrapper > div.doctor-2 h3.name {
    margin-top: 0;
  }
  .dashboard_banner .doctors-wrapper .about {
    font-size: 16px;
    line-height: 18px;
    font-weight: normal;
    padding-bottom: 16px;
    position: relative;
    color: #212127;
    margin-bottom: 16px;
  }
  #dashboard .dash-btn{
    border-radius: 20px 20px 20px 20px !important;
  }

  @media only screen and (max-width: 1240px){

    #dashboard .dashboard_banner, #dashboard #orderOnDutyWrapper {
        min-width: 100%;
        width: 100%;
    }

    #dashboard .dashboard_banner .inner.inner-center, #dashboard #orderOnDutyWrapper .inner.inner-center {
        -webkit-box-pack: justify;
        -ms-flex-pack: justify;
        justify-content: space-between;
    }
    .inner {
      width: 100%;
      padding-left: 45px;
      padding-right: 45px;
    }
  }
  @media only screen and (max-width: 1023px){
    #dashboard .left-block {
      width: 582px !important;
      margin: 0 auto 32px;
    }
    #dashboard h2.title {
      padding: 0 0 12px;
    }
    #dashboard .doctors-wrapper {
        margin: 0 auto;
    }
    #dashboard .doctors-wrapper > div.doctor-1, #dashboard .doctors-wrapper > div.doctor-2 {
      position: relative;
      padding-left: 61px;
    }

    #dashboard .doctors-wrapper > div.doctor-1:before, #dashboard .doctors-wrapper > div.doctor-2:before {
      content: "";
      position: absolute;
      width: 34px;
      height: 34px;
      background: url(/images/terapevt.png) no-repeat;
      background-size: contain;
      left: 0;
      top: 0;
      margin: 20px 0 0 14px;
    }
    #dashboard  .dashboard_banner .doctors-wrapper .price:before {
      background: none;
    }
    #dashboard .doctors-wrapper > div.doctor-1,  #dashboard .doctors-wrapper > div.doctor-2 {
      position: relative;
      padding-left: 61px;
    }
    #dashboard .doctors-wrapper > div {
      width: 282px;
      padding: 20px 14px;
    }
    #dashboard .doctors-wrapper .price,  #dashboard .doctors-wrapper .price-container {
        position: absolute;
        width: auto;
        right: 0;
        padding: 0;
        margin: 3px 14px 0 0;
        font-size: 24px;
        line-height: 24px;
    }
    #dashboard .doctor-2:before {
      background: url(/images/pediatr.png) no-repeat !important;
      background-size: contain !important;
    }
    #dashboard  .dashboard_banner .doctor-2 .price:before, #dashboard  .dashboard_banner .doctor-2 .price-container:before {
        background: none;
    }
    .dashboard_banner .doctors-wrapper .about {
      margin-bottom: 0px;
    }
  }


  @media only screen and (max-width: 765px){
    #dashboard .left-block {
        width: 100%;
        margin: 0 0 32px;
    }
    .inner {
        padding-left: 24px;
        padding-right: 24px;
    }
  }


  @media only screen and (max-width: 650px){
    .inner {
      padding-left: 10px;
      padding-right: 10px;
    }
    #dashboard .doctors-wrapper {
      width: 100%;
      margin: 0;
      -webkit-box-pack: justify;
      -ms-flex-pack: justify;
      justify-content: space-between;
    }
    #dashboard .doctors-wrapper > div {
      width: 171px;
      margin: 0;
    }
    #dashboard .doctors-wrapper > div.doctor-1, #dashboard .doctors-wrapper > div.doctor-2 {
      padding: 23px 13px 17px 14px;
      position: relative;
    }
    #dashboard .doctors-wrapper > div.doctor-1:before, #dashboard .doctors-wrapper > div.doctor-2:before {
      content: "";
      position: absolute;
      width: 34px;
      height: 34px;
      background: url(/images/terapevt.png) no-repeat;
      background-size: contain;
      left: 0;
      top: 0;
      margin: -17px 0 0 14px;
    }
    #dashboard .doctors-wrapper .price, #dashboard .doctors-wrapper .price-container {
      top: 0;
      left: 0;
      right: auto;
      margin: 56px 0 0 14px;
    }

    #dashboard .doctors-wrapper > div.doctor-1 h3.name, #dashboard .doctors-wrapper > div.doctor-2 h3.name {
      padding-bottom: 20px;
    }    
    #dashboard .doctors-wrapper .about {
      min-height: 54px;
    }
    #dashboard .doctors-wrapper > div.doctor-1,  #dashboard .doctors-wrapper > div.doctor-2 {
      padding: 23px 13px 17px 14px;
    }
    #dashboard .dash-btn {
      font-size: 12px;
    }
  }

</style>
