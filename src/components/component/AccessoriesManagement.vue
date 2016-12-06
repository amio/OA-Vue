<template>
  	<div id="CustomerManagement">
  	  <!--工具条-->	
		<el-col :span="24" class="toolbar">
			<el-form :inline="true" :model="formInline" class="demo-form-inline">
				<el-form-item>
					<el-input v-model="formInline.user" placeholder="请输入关键字"></el-input>
				</el-form-item>
				<el-form-item>
					<el-button @click="QueryBtn">查询</el-button>
				</el-form-item>
				<el-button @click="ReturnBtn" class="right">返回</el-button>
			</el-form>
			<TableOne></TableOne>
		</el-col>
	</div>	
</template>

<script>
import TableOne from './template/TableOne'
export default {
  name: 'CustomerManagement',
  data() {
      return {
        formInline: {
          user: '',
          region: ''
        }
      }
    },
    methods: {
      QueryBtn() {
        console.log('查询按钮!');
      },
      ReturnBtn() {
        console.log('返回按钮!');
      }
    },
    components: {
    	TableOne
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	#CustomerManagement{
		width:620px;
		margin:0 auto;
	}
	.right{
		float:right;
	}
</style>
