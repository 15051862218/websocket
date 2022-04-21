<template>
  <div class="login">
    <input type="text" placeholder="请输入用户名" v-model="username"/>
    <button @click="handleBtnClick">进入聊天室</button>
  </div>
</template>

<script>


export default {
  name: 'Login',
  data(){
    return{
      username:'',
    }
  },
  methods:{
    handleBtnClick(){
      const username = this.username.trim();
      if(username!='syk'){
        alert('用户不存在！');
        return;
      }else{
      localStorage.setItem('username',username);
      this.$router.push('/');
      }
      
    }
  },

  components: {
   
  }
}
</script>
