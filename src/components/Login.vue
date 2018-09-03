<template>
    <div class="login">
        <span class="zhihu-name">
            知乎
        </span>
        <div class="tip">注册知乎，发现更大的世界</div>
        <form action="shubmit">
            <div class="phone">
                <input type="text" class="phone-input" placeholder="手机号" v-model.trim="phone">
            </div>
            <div class="phone">
                <input type="password" class="phone-input" placeholder="密码" v-model.trim="password">
            </div>
            <div class="code-login">
                <a href="javascript:" class="toggle-code-login">手机验证码登陆</a>
                <a href="javascript:" class="forget-password">忘记密码</a>
            </div>
            <a href="javascript:" class="login-btn">登陆</a>
            <div class="register-org">
                <a href="javascript:" class="other-login-btn">注册机构</a>
                <span>.</span>
                <a href="javascript:" class="other-login-btn">注册机构</a>
                <span>.</span>
                <a href="javascript:" class="other-login-btn">注册机构</a>
            </div>
        </form>
        <div class="bottom">
            <span>没有账号？<a href="javascript:" @click="toggleComponent" class="toggle-register-btn">注册</a></span>
        </div>
    </div>
</template>


<script>
export default {
  name: 'Login',
  data () {
    return {
      msg: 'zhihu',
      phone:"",
      optionArray:["中国 +86","美国 +1","日本 +81"],
      selected:"中国 +86",
      password:""
    }
  },
  props:["toggleComponent"]
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
input{
    box-sizing: border-box;
    border: 0;
    outline: none;
}
a{
    text-decoration:none;
    outline: none;
}
a:hover, a:visited, a:link, a:active {
    color: black;
}
.login{
    width: 432px;
    background: #ffffff;
    position: absolute;
    left: 50%;
    top:50%;
    transform: translate(-50%,-50%);
    box-shadow: 0 1px 3px rgba(26,26,26,.1);
    border-radius: 2px;
    box-sizing: border-box;
}
.zhihu-name{
    font-size: 65px;
    color: #0084ff;
    text-align: center;
    display: block;
    margin-top: 30px;
}
.tip{
    color: #0084ff;
    text-align: center;
    font-size: 22px;
    margin-top: 15px;
    }
form{
    padding: 0 40px 36px;
    margin-top: 30px;
}    
.phone{
    height: 48px;
    border-bottom: 1px solid gray;
    padding-top: 5px;
}
.code-login{
  height: 48px;
  line-height: 48px;
  font-size: 14px;
  text-align: left;
  color:#175199;  
}
.toggle-code-login{
    line-height: 48px;
    float: left;
}
.forget-password{
    float: right;
}
#Prefix{
    width: 110px;
    color: black;
    height: 38px;
    line-height: 38px;
    font-size: 18px;
    text-align: left;
    box-sizing: border-box;
    border: 0;
    outline: none;
    float: left;
}
.sot-line{
    height: 22px;
    width: 1px;
    float: left;
    background: #ebebeb;
    margin: 12px 12px 0;
}
.phone-input{
    color: black;
    height: 38px;
    line-height: 38px;
    font-size: 18px;
    text-align: left;
    box-sizing: border-box;
    border: 0;
    outline: none;
    margin-left: 5px;
    padding-left:10px;
    overflow: hidden;
}
.code-btn{
    color: #175199;
    width: 98px;
    line-height: 48px;
    margin-left: 5px;
    float: right;
    text-align: right;
}
.souce{
    color: #175199;
    line-height: 48px;
    text-align: right;
    font-size: 14px;
    cursor:pointer;
}
.code{
    height: 48px;
    padding-top: 5px;
    font-size: 14px;
    border-bottom: 1px solid gray;
}
.code-input{
    color: black;
    height: 48px;
    line-height: 48px;
    font-size: 14px;
    text-align: left;
    box-sizing: border-box;
    border: 0;
}
a.login-btn{
    background-color: #0084ff;
    color: #ffffff;
    margin-top: 14px;
    height: 36px;
    line-height: 36px;
    width: 100%;
    display: inline-block;
    text-align: center;
}
.register-org{
    width: 100%;
    margin-top: 18px;
    font-size: 14px;
    text-align: center;
}
.register-org span{
    color: #8590a6;
}
a.other-login-btn{
    color: #175199;
}
a.toggle-register-btn{
    color:#175199;
}
.bottom{
    text-align: center;
    height: 60px;
    line-height: 60px;
    background-color: #f6f6f6;
    border-top: 1px solid #ebebeb;
    font-size: 16px;
}    
</style>
