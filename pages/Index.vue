<template>
    <div class="page-index">
        <h3>詳細情報照会ツール</h3>
        <h4>下記の検索欄で検索できます</h4>
        <div style="margin-top: 15px; margin-bottom: 15px">
          <el-input placeholder="照会項目" v-model="input3" class="input-with-select">
            <el-select v-model="select" slot="prepend" placeholder="項目種別">
              <el-option label="店舗名" value="1"></el-option>
              <el-option label="注文番号" value="2"></el-option>
              <el-option label="電話番号" value="3"></el-option>
            </el-select>
            <el-button slot="append" icon="el-icon-search" @click="searchDetail"></el-button>
          </el-input>
        </div>
        <router-link to="/detail/1">To detail page from 1</router-link>
    </div>
</template>

<script>
function setState(store) {}

export default {
    name: 'index',
    metaInfo: {
        title: 'Home',
        titleTemplate: '%s - Lavas',
        meta: [
            {name: 'keywords', content: 'lavas PWA'},
            {name: 'description', content: '基于 Vue 的 PWA 解决方案，帮助开发者快速搭建 PWA 应用，解决接入 PWA 的各种问题'}
        ]
    },
    async asyncData({store, route}) {
        setState(store);
    },
    data() {
      return {
        input3: '',
        select: ''
      }
    },
    methods: {
     searchDetail() {
       this.$router.push('/detail/' + this.input3);
     }
   }
};
</script>

<style>
.el-select .el-input {
  width: 130px;
}
.input-with-select .el-input-group__prepend {
  background-color: #fff;
}

.page-index {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

h3 {
  font-size: 36px;
  font-weight: 500;
  margin-bottom: 0;
}
</style>
