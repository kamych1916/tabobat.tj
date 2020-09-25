<template>
  <div style="background-color: #f2f3f7;">
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

    <div class="onlineConsultation-board">
      <div class="inner">
        <div>
            <div class="online-consultation-dash-container">
              <h2 class="heading">Наши сервисы</h2>
              
              <div class="service-block">

                <div class="consult-card">
                  <div class="card-content">
                    <h3>Онлайн-консультация с врачом</h3>
                    <p>Выберите удобную для себя дату и время</p>
                    <b-button class="dash-btn" variant="danger">Заказать</b-button>
                  </div>
                  <div class="circle-image-container">
                    <img src="~static/images/img-doc-circle-dash.svg" alt class="doc-circle-image" />
                  </div>
                  <!-- <button class="uk-button mobile-order-button">Заказать</button> -->
                </div>

                <div class="doctors-online-container">
                    <div class="index-item">
                      <div class="center-card">
                        <div class="infograph">
                          <div class="gray-circle">
                            <a class="icon-button margin-small-right">
                              <img src="~static/images/img-terapevt.svg" />
                            </a>
                          </div>
                        </div>
                        <div class="vertical-aligned-content">
                          <h4 class="uk-card-title">Приём в клинике</h4>
                          <p>Запись на приём в клиники Душанбе</p>
                        </div>
                      </div>
                    </div>

                    <div class="index-item">
                      <div class="center-card">
                        <div class="infograph">
                          <div class="gray-circle">
                            <a class="icon-button margin-small-right">
                              <img src="~static/images/img-pediatr.svg" />
                            </a>
                          </div>
                        </div>
                        <div class="vertical-aligned-content">
                          <h4 class="uk-card-title">Вызов на дом</h4>
                          <p>Когда нет возможности добраться до клиники</p>
                        </div>
                      </div>
                    </div>

                </div>

              </div>

            </div>
          </div>
        </div>
      </div>
    <!-- <News  /> -->
  </div>
</template>

<script>
export default {}
</script>

<style>
@import url('~static/css/index/dashboard.css');
.onlineConsultation-board .inner {
  padding-top: 30px;
}
.service-block{
  display: flex;
  /* flex-direction: column; */
  margin-top:20px
}


.consult-card {
  box-shadow: 0 15px 19px -11px rgba(32, 45, 61, 0.2);
  cursor: pointer;
  padding: 32px 52px 28px 52px;
  border-radius: 15px;
  margin-left: 0;
  outline: none;
  min-height: 244px;
  margin-bottom: 0;
  background-color: #fff;
  display: flex;
  transition: 0.2s ease-in-out;
}
.consult-card:hover{
  box-shadow: 0 15px 39px -11px rgba(32, 45, 61, 0.2);
}

.card-content {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
}
.card-content  p {
    font-size: 14px;
    font-weight: 400;
    font-style: normal;
    font-stretch: normal;
    line-height: 1.43;
    letter-spacing: normal;
    color: #6e7782;
    margin: 0;
}
.consult-card .dash-btn{
  margin-top: 20px;
  width: 150px;
}
.circle-image-container {
  display: flex;
  align-items: flex-start;
  margin-left: 20px;
}
.doc-circle-image {
  min-height: 170px;
  min-width: 170px;
  border-radius: 20rem;
  transition: 0.2s ease-in-out;
}

.doctors-online-container{
  display: flex;
  flex-direction: column;
  padding-left: 52px;
}





.index-item:first-child {
  margin-bottom: 12px;
}

.center-card {
  height: 116px;
  margin-bottom: 0;
  padding: 0 24px 0 16px;
  border-radius: 15px;
  cursor: pointer;
  /* margin-bottom: 12px; */
  min-height: 116px;
  max-width: 380px;
  box-shadow: 0 15px 19px -11px rgba(32, 45, 61, 0.2);
  background: white;
  display: flex;
  transition: 0.2s ease-in-out;
}

.center-card:hover{
  box-shadow: 0 15px 39px -11px rgba(32, 45, 61, 0.2);
}
.center-card:hover .icon-button{
  background: #bcecea;
}

.infograph{
    display: -ms-flexbox;
    display: flex;
    -ms-flex-direction: column;
    flex-direction: column;
    -ms-flex-pack: center;
    justify-content: center;
}
.gray-circle .icon-button {
    width: 68px;
    height: 68px;
    transition: .5s;
}
.icon-button {
  box-sizing: border-box;
  width: 36px;
  height: 36px;
  border-radius: 500px;
  background: #f8f8f8;
  color: #999;
  vertical-align: middle;
  display: -ms-inline-flexbox;
  display: inline-flex;
  -ms-flex-pack: center;
  justify-content: center;
  -ms-flex-align: center;
  align-items: center;
  transition: .1s ease-in-out;
  transition-property: color,background-color;
}


.margin-small-right {
    margin-right: 20px!important;
}
.center-card  p {
    font-size: 16px;
    line-height: 18px;
    font-weight: normal;
    position: relative;
    color: #212127;
    margin: 0;
}
.vertical-aligned-content{
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
