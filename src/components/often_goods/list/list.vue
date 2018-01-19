<template>
  <div>
   <el-tabs v-model="activeName2" type="card" @tab-click="handleClick">
    <el-tab-pane label="汉堡" name="first">
    <div class="jpq_bg" v-for="goods in type0Goods">
    <span class="foodImg"><img :src="goods.goodsImg" width="20%"></span>
    <span class="foodName">{{goods.goodsName}}</span>
    <span class="foodPrice">￥{{goods.price}}元</span>
    </div>

    </el-tab-pane>
    <el-tab-pane label="小吃" name="second">
    	 <div class="jpq_bg" v-for="goods in type0Goods">
       <span class="foodImg"><img :src="goods.goodsImg" width="20%"></span>
       <span class="foodName">{{goods.goodsName}}</span>
       <span class="foodPrice">￥{{goods.price}}元</span>
       </div>
    </el-tab-pane>
    <el-tab-pane label="饮料" name="third">
    	 <div class="jpq_bg" v-for="goods in type0Goods">
       <span class="foodImg"><img :src="goods.goodsImg" width="20%"></span>
       <span class="foodName">{{goods.goodsName}}</span>
       <span class="foodPrice">￥{{goods.price}}元</span>
       </div>
    </el-tab-pane>
    <el-tab-pane label="套餐" name="fourth">
    	 <div class="jpq_bg" v-for="goods in type0Goods">
       <span class="foodImg"><img :src="goods.goodsImg" width="20%"></span>
       <span class="foodName">{{goods.goodsName}}</span>
       <span class="foodPrice">￥{{goods.price}}元</span>
       </div>
    </el-tab-pane>
  </el-tabs>
    </div>
</template>

<script>
import axios from 'axios'
export default {
	components:{
		
	},
  data () {
    return {
    	activeName2: 'first',
      type0Goods:[
          {
              goodsId:1,
              goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos001.jpg",
              goodsName:'香辣鸡腿堡',
              price:18
          }, {
              goodsId:2,
              goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos002.jpg",
              goodsName:'田园鸡腿堡',
              price:15
          }, {
              goodsId:3,
              goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos004.jpg",
              goodsName:'和风汉堡',
              price:15
          }, {
              goodsId:4,
               goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos003.jpg",
              goodsName:'快乐全家桶',
              price:80
          }, {
              goodsId:5,
               goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos003.jpg",
              goodsName:'脆皮炸鸡腿',
              price:10
          }, {
              goodsId:6,
               goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos004.jpg",
              goodsName:'魔法鸡块',
              price:20
          }, {
              goodsId:7,
               goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos001.jpg",
              goodsName:'可乐大杯',
              price:10
          }, {
              goodsId:8,
               goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos003.jpg",
              goodsName:'雪顶咖啡',
              price:18
          }, {
              goodsId:9,
               goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos002.jpg",
              goodsName:'大块鸡米花',
              price:15
          }, {
              goodsId:20,
              goodsImg:"http://7xjyw1.com1.z0.glb.clouddn.com/pos002.jpg",
              goodsName:'香脆鸡柳',
              price:17
          }
          
      ]
    }
  },
  created:function(){
  	axios.get("http://jspang.com/DemoApi/oftenGoods.php")
  	.then(
  		response=>{
  			console.log(response)
//			this.type0Goods=response.data;
  		}
  	)
  	.catch(error=>{
  		console.log(error)
  	})
  },
  methods:{
  	handleClick(tab, event) {
        console.log(tab, event);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	span{
		color:#0088FB
	}
	.there{
		width:160px;
		height:20px;
		float:left;
		line-height:50px;
		padding-top:20px;
	}
	.jpq_bg{
		width:300px;
		float:left;
	}
</style>
