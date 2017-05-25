<template>
  <!--options-->
  <div class="row options-area">
    <div class="col-md-3 col-1">
      <div class="options btn-group">
        <button class="btn btn-default btn-sm dropdown-toggle" type="button" data-toggle="dropdown">
          {{size}} &nbsp;&nbsp; <span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li><a href="javascript:void(0)" v-for="item in sizeOptions" @click="selecter('size',item)">{{item}}</a></li>
        </ul>
      </div>
    </div>
    
    <div class="col-md-3 col-2">
      QYT&nbsp;&nbsp;
      
      <div class="options btn-group">
        <button class="btn btn-default btn-sm dropdown-toggle" type="button" data-toggle="dropdown">
          {{qyt}} &nbsp;&nbsp;<span class="caret"></span>
        </button>
        <ul class="dropdown-menu">
          <li><a href="javascript:void(0)" v-for="item in qytOptions" @click="selecter('qyt',item)">{{item}}</a></li>
        </ul>
      </div>
    </div>
    
    <div class="col-md-6 col-3">
      <span :style="{'color':color}">COLOR</span> &nbsp;&nbsp;
      <div class="options-color btn-group">
        <div class="color-item" v-for="item in colorOptions" :class="item.selected ? 'color-selected':''" :style="{'background-color': item.color}" @click="selecter('color',item.color,colorSelect)"></div>
      </div>
    </div>
  </div>
</template>

<script>
  import Vue from 'vue'
  export default {
    name: 'options',
    data () {
      return {
        size: 'SIZE',
        sizeOptions: ['S', 'M', 'L'],
        qyt: 1,
        qytOptions: [1, 2, 3, 4, 5],
        color: '',
        colorOptions: [
          {color: '#865970', selected: false},
          {color: '#43711D', selected: false},
          {color: '#C08C7D', selected: false},
          {color: '#899ca4', selected: false}]
      }
    },
    methods: {
      selecter(name, val, cb = null){
        this.$data[name] = val
        if (cb) cb(val)
      },
      colorSelect(val){
        for (let item of this.colorOptions) {
          if (item.color == val) {
            this.color = val
            item.selected = true
          } else {
            item.selected = false
          }
        }
      }
    }
  }
</script>

<style scoped>
  .col-1 {
    padding-left: 0;
  }
  
  .col-2 {
  
  }
  
  .col-3 {
    padding-right: 0;
  }
  
  .color-selected {
    border: 2px solid #337ab7;
  }
  
  .color-item {
    cursor: pointer;
  }
</style>
