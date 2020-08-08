<template>

    <div class="container-login">
        <div class="wrap-login">
            <b-form  style="width: 100%">

                <span class="login-form-title">
                Вход
                </span>

                <div class="wrap-input100 validate-input m-b-20 alert-validate" data-validate="Enter username or email">
                    <b-form-group
                        id="input-group-1"
                        label="Email:"
                        label-for="input-1"
                    >
                        <b-form-input
                        id="input-1"
                        v-model="username"
                        type="text"
                        required
                        placeholder="Введите email"
                        ></b-form-input>
                        <p v-if="msg.username">{{msg.username}}</p>
                    </b-form-group>
                </div>

                <div class="wrap-input100 validate-input m-b-25 alert-validate" data-validate="Enter password">
                    <b-form-group id="input-group-2" label="Пароль:" label-for="input-2">
                        <b-form-input
                        id="input-2"
                        v-model="password"
                        required
                        placeholder="Введите пароль"
                        type="password"
                        ></b-form-input>
                        <p v-if="msg.password">{{msg.password}}</p>
                    </b-form-group>
                </div>
                <div>
                    <nuxt-link v-if="resetpass" to="/reset-password" style="color: red; font-size: 0.8em">Забыли пароль?</nuxt-link>
                </div>

                <div class="text-center pt-2">
                    <b-button pill variant="info" class="px-5">Войти</b-button>
                </div>

                <!-- <div class="flex-c p-b-112">
                    <a href="#" class="login100-social-item">
                    <i class="fa fa-facebook-f"></i>
                    </a>
                    <a href="#" class="login100-social-item">
                    <img src="images/icons/icon-google.png" alt="GOOGLE">
                    </a>
                </div> -->

                <div class="text-center pt-3">
                   <nuxt-link to="/" style="color: black; font-size: 0.8em"> Нет аккаунта?</nuxt-link>
                </div>
            </b-form>
        </div>
    </div>

</template>

<script>
export default {
    layout: "empty",

    head() {
        return {
        title: "Табобат - авторизация",
        };
    },

    data: () => {
        return {
            password: null,
            msg: [],
            errorEmail: false,
            csrf: null,
            resetpass: false,
        };
    },

    methods: {

    // ФУНКЦИЯ ДЛЯ АВТОРИЗАЦИИ
        AuthReq() {
            Api.getInstance()
            .auth.login(this.username, this.password)
            .then((response) => {
                this.$router.replace({ path: "/" });
                this.csrf = "token";
            })
            .catch((error) => {
                this.$bvToast.toast("Неверное имя пользователя или пароль", {
                title: `Ошибка авторизации`,
                variant: "danger",
                solid: true,
            });
            this.resetpass = true;
        });
        },
    },

}

</script>

<style scoped>
.container-login{
    width: 100%;
    min-height: 100vh;
    display: -webkit-box;
    display: -webkit-flex;
    display: -moz-box;
    display: -ms-flexbox;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    padding: 15px;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    position: relative;
    z-index: 1;
    background-image: url('~static/images/2554504.jpg');
}
.wrap-login {
    width: 390px;
    background: #fff;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 3px 20px 0px rgba(0, 0, 0, 0.1);
    -moz-box-shadow: 0 3px 20px 0px rgba(0, 0, 0, 0.1);
    -webkit-box-shadow: 0 3px 20px 0px rgba(0, 0, 0, 0.1);
    -o-box-shadow: 0 3px 20px 0px rgba(0, 0, 0, 0.1);
    -ms-box-shadow: 0 3px 20px 0px rgba(0, 0, 0, 0.1);
    padding-right: 55px;
    padding-left: 55px;
    padding-bottom: 30px;
    padding-top: 30px;
}
.login-form-title {
    display: block;
    font-size: 30px;
    color: #4b2354;
    line-height: 1.2;
    text-align: center;
    padding-bottom: 30px;
}

</style>