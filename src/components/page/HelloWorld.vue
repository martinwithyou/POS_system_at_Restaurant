<template>
  <div class="hello">
  	 <el-row>
     <el-col :span="2">
     	<div class="grid-content bg-purple">
     	  <leftNav />
     </div>
     </el-col>
     <el-col :span="10">
     	<div class="grid-content bg-purple-light">
     		   <middle_content />
     	</div>
     </el-col>
     <el-col :span="12">
     	<div class="grid-content bg-purple">
     		   <often_goods />
     	</div>
     </el-col>
   </el-row>
  </div>
</template>

<script>
import leftNav from '../common/leftNav'
import middle_content from '../middle_content/middle_content'
import often_goods from '../often_goods/often_goods'
export default {
	components:{
		leftNav,
		middle_content,
		often_goods
	},
  data () {
    return {
     
    }
  }
}
</script>

<style>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
