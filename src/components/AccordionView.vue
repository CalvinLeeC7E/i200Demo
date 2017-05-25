<template>
  <div class="detail-area">
    <div class="detail-item" v-for="item in details">
      <div class="detail-header">
        <div class="title">{{item.title}}</div>
        <div class="options" @click="show(item)">{{item.selected ? '-' : '+'}}</div>
      </div>
      <div class="detail-content" v-if="item.selected">{{item.content}}</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'accordion_view',
    data () {
      return {
        details: [{
          title: 'DETAIL',
          selected: true,
          content: 'Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula elementum sed sit amet dui. Vivamus suscipit tortor eget felis porttitor volutpat.'
        }, {
          title: 'DELIVERY',
          selected: false,
          content: 'Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula elementum sed sit amet dui. Vivamus suscipit tortor eget felis porttitor volutpat.'
        }, {
          title: 'STYLE',
          selected: false,
          content: 'Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula elementum sed sit amet dui. Vivamus suscipit tortor eget felis porttitor volutpat.'
        }, {
          title: 'STYLE',
          selected: false,
          content: 'Curabitur arcu erat, accumsan id imperdiet et, porttitor at sem. Vestibulum ac diam sit amet quam vehicula elementum sed sit amet dui. Vivamus suscipit tortor eget felis porttitor volutpat.'
        }]
      }
    },
    methods: {
      show(itemObj){
        for (let item of this.details) {
          if(item == itemObj){
            item.selected = !item.selected
          }else{
            item.selected = false
          }
        }
      }
    }
  }
</script>

<style scoped>
  .detail-area {
    margin-top: 50px;
  }
  
  .detail-header {
    width: 100%;
    display: inline-table;
    padding: 10px 0;
    border-bottom: 2px solid #f6f6f6;
  }
  
  .title {
    font-size: 1.2em;
    float: left;
  }
  
  .options {
    font-size: 1.5em;
    float: right;
    cursor: pointer;
    color: #d3995f;
  }
  
  .detail-content {
    padding: 30px 0;
    line-height: 2.0;
    color: #686868;
  }
</style>
