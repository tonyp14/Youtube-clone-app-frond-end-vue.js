<template>
  <div>
    <nav class="navbar navbar-default">
      <div class="container-fluid tab">
        <div class="navbar-header">
          <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#myNavbar">
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
          </button>
          <a class="navbar-brand" :href="urlhome">
            <img src="../assets/tec.png" class="logo">
          </a>
        </div>
        <div class="collapse navbar-collapse" id="myNavbar">
          <ul class="nav navbar-nav navbar-right">
            <li><a :href="urlsignup"><span class="glyphicon glyphicon-user"></span> Signup</a></li>
            <li><a href="#"><span class="glyphicon glyphicon-log-in"></span> Signin</a></li>
          </ul>
        </div>
      </div>
    </nav>
    <div class="container-fluid">
      <div class="row">
        <div class="col-lg-4 col-md-3 col-sm-2 col-xs-1"></div>
        <div class="col-lg-4 col-md-6 col-sm-8 col-xs-10">
          <div class="row box">
            <div class="cover">
              <div class="row">
                <div class="col-md-12 col-sm-12 col-xs-12 col-lg-12">
                    <center>
                      <img src="../assets/sin.png" class="icon">
                    </center>
                </div>
              </div>
               <div class="row">
                  <div class="col-md-12 col-sm-12 col-xs-12 col-lg-12">
                    <div class="row">
                      <div class="col-md-3 col-sm-3 col-xs-5 col-lg-6">
                        <div class="header email">Email</div>
                      </div>
                    </div>
                    <center>
                      <input id="email" class="letter" type="text" v-model="email" placeholder="example@gmail.com" value=""/><br>
                    </center>
                    <div class="row">
                      <div class="col-md-3 col-sm-3 col-xs-5 col-lg-6">
                        <div class="header">Password</div>
                      </div>
                    </div>
                    <center>
                      <input id="pw"  class="letter" type="password" v-model="pswd" placeholder="Password" value=""/>
                    </center>
                    <br>
                      <div class="row">
                        <div class="col-md-1 col-sm-1 col-xs-1 col-lg-1">
                          <label  class="container">
                            <div class="check">
                              <input v-on:click="view()" type="checkbox" name="gra">
                                <span class="checkmark"></span>
                            </div>
                          </label>
                        </div>
                        <div class="col-md-6 col-sm-8 col-xs-9 col-lg-5">
                          <div class="show">Show Password</div>
                        </div>
                      </div>
                    <center>
                      <div class="btn_lg" v-on:click="signin()">
                        signin
                      </div>
                    </center>
                  </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-lg-4 col-md-3 col-sm-2 col-xs-1"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'login',
  data () {
    return {
      email: '',
      pswd: '',
      urlsignup: '#/s',
      urlhome: '#/ls'
    }
  },
  methods: {
    view: function () {
      var x = document.getElementById('pw')
      if (x.type === 'password') {
        x.type = 'text'
      } else {
        x.type = 'password'
      }
    },
    signin: function () {
      var em = this.email
      var pw = this.pswd
      alert(em)
      alert(pw)
    }
  }
}
</script>
<style scoped>
  .logo {
    width: 95%;
    height: 75px;
    margin-top: -12px;
    margin-left: 25px;
  }

  .tab {
    border-radius: 0px;
    border-radius: 0px;
    background-color: #fff;
    height: 85px;
    margin-top: -61px;
    box-shadow: 0px 5px 5px #e7e7e7;
  }

  .navbar-default {
    background-color: #fff;
    border-color: #fff;
  }

  .navbar-right {
    float: right!important;
    margin-right: -15px;
    margin-top: 15px;
    font-size: 1.3em;
  }

  .navbar-nav>li>a {
    color: #ff7517;
  }

  .active {
    color: #252422;
  }

  .navbar-toggle {
    border-color: #ff7517;
    margin-top: 25px;
  }
  .box {
    margin-top: 8%;
  }

  .cover {
    padding: 30px;
    box-shadow: 0 6px 8px 0 rgba(0,0,0,0.2);
    transition: 0.3s;
    width: 85%;
    margin: auto;
  }

  .btn_lg {
    margin-top: 35px;
    padding-top: 5%;
    color:#fff;
    background-color: #ff7517;
    width: 90%;
    height: 46px;
    font-size: 23px;
    text-align: center;
    padding-top: 6px;
    border-radius: 2px;
    font-family: 'Slack-Lato','Roboto',Arial, Helvetica, sans-serif;
    box-shadow: 0 6px 10px 0 rgba(0,0,0,0.3);
    cursor: pointer;
    transition: 0.3s;
    margin-bottom: 25px;
  }

  .icon {
    width: 45%;
    height: 50px;
    margin-bottom: 35px;
    margin-top: 10px;
  }

  label {
    display: inline-block;
    max-width: 100%;
    margin-bottom: 0px;
    font-weight: 700;
    margin-top: 20px;
  }

  .letter {
    padding-left: 20px;
    height: 3.3em;
    width: 90%;
    margin-top: .2em;
    border-radius: 1px;
    border: 2px solid #eeeeee
  }

  @media screen and (min-width: 300px) and (max-device-width: 455px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: 12%;
    }
    .email {
      margin-left: -16%;
    }
  }

  @media screen and (min-width: 456px) and (max-device-width: 599px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: -8%;
    }
    .email {
      margin-left: -35%;
    }
  }

  @media screen and (min-width: 600px) and (max-device-width: 767px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: -22%;
    }
    .email {
      margin-left: -43%;
    }
  }

  @media screen and (min-width: 768px) and (max-device-width: 799px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: 28%;
    }
    .email {
      margin-left: 0%;
    }
  }

  @media screen and (min-width: 800px) and (max-device-width: 999px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: 27%;
    }
    .email {
      margin-left: 0%;
    }
  }

  @media screen and (min-width: 1000px) and (max-device-width: 1199px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: 24%;
    }
    .email {
      margin-left: 0%;
    }
  }

  @media screen and (min-width: 1200px) and (max-device-width: 1249px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: -20%;
    }
    .email {
      margin-left: -42%;
    }
  }

  @media screen and (min-width: 1250px) and (max-device-width: 1600px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: -24%;
    }
    .email {
      margin-left: -45%;
    }
    .show {
      left: 30px;
      position: absolute;
      top: 20px;
      }
  }

    @media screen and (min-width: 1601px) and (max-device-width: 2000px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: -38%;
    }
    .email {
      margin-left: -54%;
    }
    .show {
      left: 30px;
      position: absolute;
      top: 20px;
      }
  }

      @media screen and (min-width: 2001px) and (max-device-width: 2600px) {
    .header {
      display: inline-block;
      margin-bottom: 0px;
      font-weight: 600;
      letter-spacing: 1px;
      margin-top: 30px;
      margin-left: -51%;
    }
    .email {
      margin-left: -64%;
    }
    .checkmark {
      position: absolute;
      top: 0;
      left: 33px;
      height: 20px;
      width: 20px;
      background-color: #fff;
      border: 1px solid #ff7517;
    }
    .show {
      left: 30px;
      position: absolute;
      top: 20px;
      }
  }
  .show {
    left: 30px;
    position: absolute;
    top: 20px;
    font-weight: 500;
    letter-spacing: 1px;
  }
  .check {
  padding-top: 7px;
  padding-bottom: 7px;
  padding-left: 6px;
  }

  .container {
    display: block;
    position: relative;
    padding-left: 23px;
    margin-bottom: 3px;
    cursor: pointer;
    font-size: 12px;
    font-family: 'Roboto',Arial, Helvetica, sans-serif;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    user-select: none;
  }

  .container input {
    position: absolute;
    opacity: 0;
    cursor: pointer;
  }

  .checkmark {
    position: absolute;
    top: 0;
    left: 21px;
    height: 20px;
    width: 20px;
    background-color: #fff;
    border: 1px solid #ff7517;
  }

  .container:hover input ~ .checkmark {
    background-color: #ff7517;
  }

  .container input:checked ~ .checkmark {
    background-color: #fff;
  }

  .checkmark:after {
    content: "";
    position: absolute;
    display: none;
  }

  .container input:checked ~ .checkmark:after {
    display: block;
  }

  .container .checkmark:after {
    left: 5px;
    top: 4px;
    width: 6px;
    height: 9px;
    border: solid #ff7517;
    border-width: 0 3px 3px 0;
    -webkit-transform: rotate(55deg);
    -ms-transform: rotate(45deg);
    transform: rotate(45deg);
  }

</style>
