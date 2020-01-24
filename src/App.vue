<template>
  <div id="app">

    <!-- <van-list v-model="loading" finished = "finished" finished-text="没有更多了" @load="onLoad"> -->
      <div v-for="content in list" :key="content.name">
        <van-cell
          title="医院名称"
          :value="content.name"
        />
        <van-cell
          title="医院地址"
          :value="content.address"
        />
        <van-cell
          title="联系人"
          :value="content.contat"
        />
        <van-cell
          title="联系电话"
          :value="content.mobile"
        />
        <div style="color: #000; font-size: 16px">物资清单</div>
        <div v-for="item in content.items" :key="item.name" style="border: 1px solid #000010; margin: 20px; font-size: 10px">
          <van-cell
            title="物资名称"
            :value="item.name"
          />
          <van-cell
            title="物资数量"
            :value="item.amount"
          />
          <van-cell
            title="物资单位"
            value="盒"
          />
        </div>
      </div>
    <!-- </van-list> -->
  </div>
</template>

<script>

import Vue from 'vue';
import { Col, Row, Cell } from 'vant';

Vue.use(Col);
Vue.use(Row);
Vue.use(Cell);



export default {
  name: 'app',
  components: {

  },
  data() {
    return {
      list: [
        {
          no: 1,
          name: "武汉大学任命医院",
          address: "湖北省武汉市武昌区解放路238号",
          contat: "刘老师",
          mobile: 13146228147,
          items: [
            {
              name: "N95口罩",
              amount: 10
            },
            {
              name: "外科口罩",
              amount: 100
            },
            {
              name: "一次性口罩",
              amount: 10202
            }
          ]
        },
        {
          no: 1,
          name: "武汉大学任命医院",
          address: "湖北省武汉市武昌区解放路238号",
          contat: "刘老师",
          mobile: 13146228147,
          items: [
            {
              name: "N95口罩",
              amount: 10
            },
            {
              name: "外科口罩",
              amount: 100
            },
            {
              name: "一次性口罩",
              amount: 10202
            }
          ]
        },
        {
          no: 1,
          name: "武汉大学任命医院",
          address: "湖北省武汉市武昌区解放路238号",
          contat: "刘老师",
          mobile: 13146228147,
          items: [
            {
              name: "N95口罩",
              amount: 10
            },
            {
              name: "外科口罩",
              amount: 100
            },
            {
              name: "一次性口罩",
              amount: 10202
            }
          ]
        },
        {
          no: 1,
          name: "武汉大学任命医院",
          address: "湖北省武汉市武昌区解放路238号",
          contat: "刘老师",
          mobile: 13146228147,
          items: [
            {
              name: "N95口罩",
              amount: 10
            },
            {
              name: "外科口罩",
              amount: 100
            },
            {
              name: "一次性口罩",
              amount: 10202
            }
          ]
        },
        {
          no: 1,
          name: "武汉大学任命医院",
          address: "湖北省武汉市武昌区解放路238号",
          contat: "刘老师",
          mobile: 13146228147,
          items: [
            {
              name: "N95口罩",
              amount: 10
            },
            {
              name: "外科口罩",
              amount: 100
            },
            {
              name: "一次性口罩",
              amount: 10202
            }
          ]
        }
      ],
      loading: false,
      finished: true
    }
  },
  methods: {
    onLoad() {
      // 异步更新数据
      // setTimeout(() => {
      //   // for (let i = 0; i < 10; i++) {
      //   //   this.list.push(this.list.length + 1);
      //   // }
      //   // 加载状态结束
      //   this.loading = false;

      //   // 数据全部加载完成
      //   if (this.list.length >= 40) {
      //     this.finished = true;
      //   }
      // }, 500);
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
