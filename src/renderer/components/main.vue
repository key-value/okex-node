<template>
  <el-container style="height:100vh; border: 1px solid #eee">
    <el-header style="text-align: right; font-size: 12px">
      <el-row>
        <el-button type="primary">导入</el-button>
        <el-button type="success">启动</el-button>
      </el-row></el-header
    >
    <el-main
      ><el-row>
        <div id="cardList">
          <el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>btc-usdt</span>
            </div>
            <div>
              {{ "列表内容 " }}
            </div> </el-card
          ><el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>eth-btc</span>
            </div>
            <div>
              {{ "列表内容 " }}
            </div> </el-card
          ><el-card class="box-card">
            <div slot="header" class="clearfix">
              <span>eth-usdt</span>
            </div>
            <div>
              {{ "列表内容 " }}
            </div>
          </el-card>
        </div></el-row
      >
      <el-table :data="tableData">
        <el-table-column
          prop="date"
          label="btc-usdt"
          width="140"
        ></el-table-column>
        <el-table-column
          prop="name"
          label="eth-btc"
          width="140"
        ></el-table-column>
        <el-table-column
          prop="address"
          label="eth-usdt"
          width="140"
        ></el-table-column>
      </el-table>
    </el-main>
  </el-container>
</template>
<style lang="scss" scoped>
.el-header {
  background-color: #b3c0d1;
  color: #333;
  line-height: 60px;
}

.el-aside {
  color: #333;
}

.item {
  margin-bottom: 18px;
}

.clearfix:before,
.clearfix:after {
  display: table;
  content: "";
}
.clearfix:after {
  clear: both;
}

#cardList {
  display: flex;
}
.box-card {
  margin: 0 5px;
  // width: 320px;
  flex-grow: 1;
  justify-content: center;
}
.el-card /deep/ .el-card__body {
  font-size: 12px;
  padding: 13px;
}
</style>
<script>
export default {
  data() {
    const item = {
      date: "2016-05-02",
      name: "王小虎",
      address: "上海市普陀",
    };
    return {
      tableData: Array(3).fill(item),
    };
  },
};
</script>
