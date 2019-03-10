<template>
  <div>
    <el-row class="table-wrap">
      <el-col :span="24">
        <el-table
          :data="tableList"
          :cell-style="cellStyle"
          :header-cell-style="cellStyle"
          class="table"
          :row-class-name="tableRowClassName"
        >
          <el-table-column
            align="center"
            v-for="col in columns"
            :prop="col.prop"
            :key="col.prop"
            :label="col.label"
            :width="col.width"
          ></el-table-column>
        </el-table>
      </el-col>
      <el-col :span="12"></el-col>
    </el-row>
  </div>
</template>
<script>
export default {
  layout: 'classic',
  data() {
    return {
      tableList: [
        {
          name: '张三',
          age: 28
        },
        {
          name: '李四',
          age: 24
        }
      ],
      columns: [
        {
          prop: 'name',
          label: '名称'
        },
        {
          prop: 'age',
          label: '年龄'
        }
      ]
    }
  },
  methods: {
    cellStyle({ row, column, rowIndex, columnIndex }) {
      console.log(row.name)
      return 'color:blue;border:1px solid black;padding:0;height:40px;box-sizing:content-box;'
    },
    tableRowClassName({ row, rowIndex }) {
      // console.log(row)
      // console.log(rowIndex)
      if (rowIndex % 2 === 0) {
        return 'success-row'
      }
      return 'warning-row'
    }
  }
}
</script>
<style lang="scss" >
.table-wrap {
  width: 70vw;
  margin: 0 auto;
  padding-top: 50px;
  .table {
    padding: 10px 0;
    border-collapse: collapse;
  }
  table {
  }
  // .el-table__body,
  // .el-table__header {
  //   border-collapse: collapse;
  // }

  .el-table {
    .warning-row {
      background: green;
    }
    .success-row {
      background: red;
    }
  }
}
</style>
