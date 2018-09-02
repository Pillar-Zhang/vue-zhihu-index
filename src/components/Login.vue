<template>
    <div class="login">
        <span class="zhihu-name">
            知乎
        </span>
        <div class="tip">注册知乎，发现更大的世界</div>
        <form action="shubmit">
            <div class="phone">
                <select name="" id="Prefix" v-model="selected" >
                    <option :value="option" v-for="option in optionArray" :key="option">{{option}}</option>
                </select>
                <span class="sot-line"></span>
                <input type="text" class="phone-input" placeholder="手机号" v-model="phone">
            </div>
            <div class="code">
                <input type="text" class="code-input" placeholder="输入六位短信验证码" v-model="code">
                <a href="javascript:" class="code-btn">获取短信验证码</a>
            </div>
            <div class="souce">接受语音验证码</div>
            <a href="javascript:" class="register-btn">注册</a>
        </form>
        
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
      code:""
    }
  }
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
}
.zhihu-name{
    font-size: 65px;
    color: #0084ff;
    text-align: center;
    display: block;
    margin-top: 30%;
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
}
.souce{
    color: #175199;
    line-height: 48px;
    text-align: right;
}
.code{
    height: 48px;
    padding-top: 5px;
    font-size: 16px;
    border-bottom: 1px solid gray;
}
.code-input{
    color: black;
    height: 38px;
    line-height: 38px;
    font-size: 16px;
    text-align: left;
    box-sizing: border-box;
    border: 0;
}
a.register-btn{
    background-color: #0084ff;
    color: #ffffff;
    margin-top: 30px;
    height: 36px;
    line-height: 36px;
    width: 100%;
    display: inline-block;
    text-align: center;
}    
</style>
