<template>
  <div class="left-nav">
        <div class="choice_part">
            <i class="icon iconfont icon-toys"></i>
            <div>收银</div>
        </div>
        <div class="choice_part">
            <i class="icon iconfont icon-toys"></i>
            <div>店铺</div>
       </div>
        <div class="choice_part">
            <i class="icon iconfont icon-toys"></i>
            <div>商品</div>
        </div>
        <div class="choice_part">
            <i class="icon iconfont icon-toys"></i>
            <div>会员</div>
        </div>
        <div class="choice_part">
            <i class="icon iconfont icon-toys"></i>
            <div>统计</div>
        </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: 'Welcome POS'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.choice_part{
		width:100%;
		height:60px;
		margin-top:20px;
		margin-bottom:20px;
	}
    .left-nav{
       color:#fff;
       font-size:10px;
       height:100%;
       background-color: #1D8ce0;
       float:left;
       width:65px;
    }

    .iconfont{
       font-size:24px;
    }
    li{
    	width:65px;
    	color:#888888;
    	margin:0px;
    	color:#ffffff;
    }
    .left-nav ul{
        padding:0px;
        margin: 0px;
    }
    .left-nav li{
        list-style: none;
        text-align: center;
        border-bottom:1px solid #20a0ff;
        padding:10px;
    }
</style>
