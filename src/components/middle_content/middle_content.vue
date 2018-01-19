<template>
  <div>
  <el-tabs v-model="activeName">
    <el-tab-pane label="结账" name="first">
    	<table1/>
    </el-tab-pane>
    <el-tab-pane label="挂单" name="second">
    	<table2/>
    </el-tab-pane>
    <el-tab-pane label="外卖" name="third">
    	<table3/>
    </el-tab-pane>
  </el-tabs>
  </div>
</template>

<script>
import table3 from './tables/table3'
import table2 from './tables/table2'
import table1 from './tables/table1'
export default {
	components:{
		table3,
		table2,
		table1
	},
  data () {
    return {
      activeName: 'first'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	
</style>
