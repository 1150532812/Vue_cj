<template>
  <div id="user">
    <el-container >
      <el-main>
        <el-breadcrumb separator="/">
          <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
          <el-breadcrumb-item>用户中心</el-breadcrumb-item>
        </el-breadcrumb>
        <el-dropdown>
          <i class="el-icon-setting" ></i>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>查看</el-dropdown-item>
            <el-dropdown-item>新增</el-dropdown-item>
            <el-dropdown-item>删除</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
        <span>选择要操作的类型</span>
        <el-table :data="tableData">
          <el-table-column prop="date" label="日期" width="140">
          </el-table-column>
          <el-table-column prop="name" label="姓名" width="120">
          </el-table-column>
          <el-table-column prop="address" label="地址">
          </el-table-column>
        </el-table>
      </el-main>
      </el-container>
    <div class="button">
      <el-row>
        <el-button type="success">操作成功</el-button>
        <el-button type="warning">警告</el-button>
        <el-button type="danger">危险</el-button>
      </el-row>
    </div>
  </div>

</template>

<script>
export default {
  name: 'User',
  data () {
    const item = {
      date: '2016-05-02',
      name: '王小虎',
      address: '上海市普陀区金沙江路 1518 弄'
    }
    return {
      tableData: Array(10).fill(item)
    }
  }
}
</script>
<style scoped>
.button{
  margin: 600px 0 0 200px;
}
.el-main{
  /*margin: 80px 0 0 200px;*/
}
.el-dropdown{
  margin-right: 15px;
}
.el-breadcrumb{
  margin: 0 0 0 200px;
}
.el-aside {
  color: #333;
}
</style>
