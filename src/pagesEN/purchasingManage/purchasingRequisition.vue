<template lang="html">
  <div id="container">
    <div class="views-container">
      <div class="views-title">
        <ul class="clearfix">
          <li class="active">Procurement List</li>
        </ul>
      </div>
      <div class="container-right">
        <div class="search-div">
          <span>ABC Type：</span>
          <el-select size="small" class="tableSearchInput" value="All" placeholder="Please Select"><el-option value='All'></el-option></el-select>
          <span class="ml20">Key：</span>
          <el-input class='tableSearchInput' size="small"  placeholder="" icon="search"></el-input>
          <span class="ml20">Date range：</span> 
          <el-date-picker v-model="value7" size="small" type="daterange" align="left"  :picker-options="pickerOptions2" start-placeholder="Start date"  end-placeholder="End date"></el-date-picker>
          <div class="fr mt15">
            <button class="export" size="small"><i class="icon_export"></i>Export</button>
          </div>
        </div>
        <el-table ref="multipleTable" :data="tableData3" stripe tooltip-effect="dark" style="width: 100%">
          <el-table-column type="selection" width="55" align="center"></el-table-column>
          <el-table-column prop="order" label="Order" align="center"></el-table-column>
          <el-table-column prop="code" label="Item Number" align="center"></el-table-column>
          <el-table-column prop="name" label="Item Name" align="center"></el-table-column>
          <el-table-column prop="ccc" label="Second Attribute" align="center"></el-table-column>
          <el-table-column prop="property" label="ABC Type" align="center"></el-table-column>
          <el-table-column prop="types" label="Model" align="center"></el-table-column>
          <el-table-column prop="type" label="Standards" align="center"></el-table-column>
          <el-table-column prop="manager" label="Count" align="center"></el-table-column>
          <el-table-column prop="aaa" label="Price" align="center"></el-table-column>
          <el-table-column prop="bbb" label="Total Price" align="center"></el-table-column>
          <el-table-column prop="ccc" label="Reference Price" align="center"></el-table-column>
          <el-table-column prop="ddd" label="Discount Price" align="center"></el-table-column>
          <el-table-column prop="eee" label="Fluctuation" align="center"></el-table-column>
          <el-table-column prop="fff" label="Fixed Lead Time" align="center"></el-table-column>
          <el-table-column prop="ggg" label="BL Date" align="center"></el-table-column>
          <el-table-column prop="hhh" label="Procured By" align="center"></el-table-column>
          <el-table-column prop="iii" label="Department" align="center"></el-table-column>
        </el-table>
        <div style="margin-top: 20px">
          <el-button size="small" type="primary" icon="plus">Add</el-button>
          <el-button size="small" type="primary" icon="edit" class="el-button--edit">Edit</el-button>
          <el-button size="small" type="danger" icon="close">Delete</el-button>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        input:'',
        value7: '',
        pickerOptions2: {
          shortcuts: [{
            text: 'Last Week',
            onClick(picker) {
              const end = new Date();
              const start = new Date();
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 7);
              picker.$emit('pick', [start, end]);
            }
          }, {
            text: 'Last Month',
            onClick(picker) {
              const end = new Date();
              const start = new Date();
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 30);
              picker.$emit('pick', [start, end]);
            }
          }, {
            text: 'Last 3 months',
            onClick(picker) {
              const end = new Date();
              const start = new Date();
              start.setTime(start.getTime() - 3600 * 1000 * 24 * 90);
              picker.$emit('pick', [start, end]);
            }
          }]
        },
        tableData3: [{
          order: '1',
          code: 'DQ-JS0087',
          name: 'Charging panel',
          property: 'A',
          types:'A8',
          type: 'A8/70g',
          manager: '30',
          aaa: '50.00',
          bbb: '1500.00',
          ccc: '-',
          ddd: '-',
          eee: '-',
          fff: '-',
          ggg: '09-22 15:07',
          hhh: 'Mr Xiang',
          iii: 'Technology dept',
        }, {
          order: '2',
          code: 'DQ-JS0087',
          name: 'Charging panel',
          property: 'A',
          types:'A8',
          type: 'A8/70g',
          manager: '30',
          aaa: '50.00',
          bbb: '1500.00',
          ccc: '-',
          ddd: '-',
          eee: '-',
          fff: '-',
          ggg: '09-22 15:07',
          hhh: 'Mr Xiang',
          iii: 'Technology dept',
        }, {
          order: '3',
          code: 'DQ-JS0087',
          name: 'Charging panel',
          property: 'A',
          types:'A8',
          type: 'A8/70g',
          manager: '30',
          aaa: '50.00',
          bbb: '1500.00',
          ccc: '-',
          ddd: '-',
          eee: '-',
          fff: '-',
          ggg: '09-22 15:07',
          hhh: 'Mr Xiang',
          iii: 'Technology dept',
        }, {
          order: '4',
          code: 'DQ-JS0087',
          name: 'Charging panel',
          property: 'A',
          types:'A8',
          type: 'A8/70g',
          manager: '30',
          aaa: '50.00',
          bbb: '1500.00',
          ccc: '-',
          ddd: '-',
          eee: '-',
          fff: '-',
          ggg: '09-22 15:07',
          hhh: 'Mr Xiang',
          iii: 'Technology dept',
        }],
        multipleSelection: []
      };
    },mounted:function(){
      this.$nextTick(function() {
          this.doRandom();
      })
    },
    methods:{
      doRandom(){
        const that = this,
              end = new Date(),
              start = end.getTime() - 3600 * 1000 * 24 * 7;
        that.value7 = [start,end];      
      }
    }
  };
</script>
<style lang="scss" scoped>
  .views-container{
    width: 100%;
    
    .tableSearchInput{
    	width: 150px;
    }
  }
  .container-right{
    padding:0 20px
  }
  .tableSearchInput{
    width: 250px;
    margin: 15px 0 ;
  }
</style>