<template>
  <div class="toEvaluate">
    <nav-bar class="cartNavBar" ref="cartNavBar">
      <div slot="left" class="left" v-on:click="$router.go(-1)">
        <i class="el-icon-arrow-left"></i>
      </div>
      <div slot="center">
        <div class="title" style="line-height:44px">评价晒单</div>
      </div>
      <div slot="right" class="right">
        <el-dropdown trigger="click" @command="pushRouter">
          <span class="el-dropdown-link">
            <i class="el-icon-more-outline el-icon-more"></i>
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item command="/home">首页</el-dropdown-item>
            <el-dropdown-item command="/keywords">分类搜索</el-dropdown-item>
            <el-dropdown-item command="/profile">我的京东</el-dropdown-item>
            <el-dropdown-item command="/profile" disabled>浏览记录</el-dropdown-item>
            <el-dropdown-item command="/profile" divided>我的关注</el-dropdown-item>
            <el-dropdown-item command="/profile" divided>分享</el-dropdown-item>
          </el-dropdown-menu>
        </el-dropdown>
      </div>
    </nav-bar>

    <!-- 商品评分 -->
    <div class="shopRating">
      <div>
        <div v-for="(item,index) in EvaluateData" :key="index" style="float:left">
          <img :src="path+item.img_cover" alt class="shopImg" />
        </div>
        <p>商品评分</p>
      </div>

      <div class="star" v-for="(i) in list" :key="i">
        <div @click="shopRating(i)">
          <img :src="xing>i?starN:starY" />
        </div>
      </div>
    </div>

    <div class="big_box">
      <div style="float:left;width:100%;background:#fff">
        <el-input
          type="textarea"
          placeholder="评论大于超过20元的商品超过10个字就有机会获得京豆"
          v-model="textarea"
          maxlength="500"
          show-word-limit
        ></el-input>
        <p class="add" style="text-align:left;margin-left:20px;">添加视频/图片(0/9)</p>

        <div style="width:100%;float:left;margin-bottom:20px">
          <div style="float:left">
            <el-upload action="#" list-type="picture-card" :auto-upload="false">
              <i slot="default" class="el-icon-video-camera-solid">
                <p style="font-size:10px">添加视频</p>
              </i>
              <div slot="file" slot-scope="{file}">
                <img class="el-upload-list__item-thumbnail" :src="file.url" alt />
                <span class="el-upload-list__item-actions">
                  <span
                    class="el-upload-list__item-preview"
                    @click="handlePictureCardPreview(file)"
                  >
                    <i class="el-icon-video-camera-solid"></i>
                  </span>
                  <span
                    v-if="!disabled"
                    class="el-upload-list__item-delete"
                    @click="handleDownload(file)"
                  >
                    <i class="el-icon-download"></i>
                  </span>
                  <span
                    v-if="!disabled"
                    class="el-upload-list__item-delete"
                    @click="handleRemove(file)"
                  >
                    <i class="el-icon-delete"></i>
                  </span>
                </span>
              </div>
            </el-upload>
            <el-dialog :visible.sync="dialogVisible">
              <img width="100%" :src="dialogImageUrl" alt />
            </el-dialog>
          </div>

          <div style="float:left">
            <el-upload action="#" list-type="picture-card" :auto-upload="false">
              <i slot="default" class="el-icon-camera-solid">
                <p style="font-size:10px">添加图片</p>
              </i>

              <div slot="file" slot-scope="{file}">
                <img class="el-upload-list__item-thumbnail" :src="file.url" alt />
                <span class="el-upload-list__item-actions">
                  <span
                    class="el-upload-list__item-preview"
                    @click="handlePictureCardPreview(file)"
                  >
                    <i class="el-icon-zoom-in"></i>
                  </span>
                  <span
                    v-if="!disabled"
                    class="el-upload-list__item-delete"
                    @click="handleDownload(file)"
                  >
                    <i class="el-icon-download"></i>
                  </span>
                  <span
                    v-if="!disabled"
                    class="el-upload-list__item-delete"
                    @click="handleRemove(file)"
                  >
                    <i class="el-icon-delete"></i>
                  </span>
                </span>
              </div>
            </el-upload>
            <el-dialog :visible.sync="dialogVisible">
              <img width="100%" :src="dialogImageUrl" alt />
            </el-dialog>
          </div>
        </div>
        <p style="text-align:left;margin-left:20px">
          <input type="checkbox" />
          匿名发布
          <span style="float:right;font-size:10px;color:grey;margin-right:20px">投稿说明</span>
        </p>
      </div>

      <!-- 物流服务 -->
      <div class="service">
        <p class="wuliu">物流服务评价</p>
        <span class="pj">
          评价大于200元的订单可获得10京豆
          <br />(订单完成3个月内有效)
        </span>
        <div style="width: 100%;float: left;">
          <p style="float:left;margin-left:20px;padding-right:13%">快递包装</p>
          <div class="star" v-for="(i) in list" :key="i">
            <div @click="pack(i)">
              <!--快递包装-->
              <img :src="packStar>i?starN:starY" />
            </div>
          </div>
        </div>

        <div style="width: 100%;float: left;">
          <p style="float:left;margin-left:20px;padding-right:13%">送货速度</p>
          <div class="star" v-for="(i) in list" :key="i">
            <div @click="speed(i)">
              <!--送货速度-->
              <img :src="speedStar>i?starN:starY" />
            </div>
          </div>
        </div>

        <div style="width: 100%;float: left;">
          <p style="float:left;margin-left:20px;padding-right:9%">配送员服务</p>
          <div class="star" v-for="(i) in list" :key="i">
            <div @click="DisService(i)">
              <!--配送员服务-->
              <img :src="DisServiceStar>i?starN:starY" />
            </div>
          </div>
        </div>

        <el-button type="danger">提交</el-button>
        <div>
          <p style="font-size:14px">评价晒图功能均能获得京豆奖励!</p>
          <span style="font-size: 12px;color: red;">详细奖励规则</span>
        </div>
        <img src="../../images/logo.png" alt style="width: 100px;
    margin-top: 20px;" />
      </div>
    </div>
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar";
import { getGoodsId } from "network/goods";
export default {
  name: "toEvaluate",
  data() {
    return {
      path: "http://106.12.85.17:8090/public/image/goods/",
      EvaluateData: [],
      list: [0, 1, 2, 3, 4],
      starY: require("@/assets/img/details/xxy.png"), //亮星星
      starN: require("@/assets/img/details/xxn.png"), //暗星星
      xing: 0,
      packStar: 0, //快递包装
      speedStar: 0, //送货速度
      DisServiceStar: 0, //配送员服务
      text: "",
      textarea: "",
      dialogImageUrl: "",
      dialogVisible: false,
      disabled: false
    };
  },
  components: {
    NavBar
  },
  computed: {},
  created() {
    console.log(this.$route.params.id);
    this.getGoodsId();
  },
  activated() {},
  deactivated() {},
  mounted() {},
  methods: {
    pushRouter(path) {
      this.$router.push(path);
    },
    getGoodsId() {
      getGoodsId(this.$route.params.id).then(res => {
        console.log(res.data.goodsData);
        this.EvaluateData.push(res.data.goodsData);
        console.log(this.EvaluateData);
      });
    },
    shopRating(val) {
      this.xing = val + 1;
      console.log("点击了" + (val + 1) + "颗星");
    },
    pack(val) {
      this.packStar = val + 1;
      console.log("点击了" + (val + 1) + "颗星");
    },
    speed(val) {
      this.speedStar = val + 1;
      console.log("点击了" + (val + 1) + "颗星");
    },
    DisService(val) {
      this.DisServiceStar = val + 1;
    },
    handleRemove(file) {
      console.log(file);
    },
    handlePictureCardPreview(file) {
      this.dialogImageUrl = file.url;
      this.dialogVisible = true;
    },
    handleDownload(file) {
      console.log(file);
    }
  }
};
</script>
<style lang='less'>
.toEvaluate {
  .shopRating {
    width: 100%;
    border-bottom: 1px solid #dedede;
    height: 70px;
    img.shopImg {
      width: 50px;
      height: auto;
      padding: 15px 10px;
      display: block;
    }
    p {
      font-size: 16px;
      float: left;
      line-height: 40px;
    }
    .star {
      width: 30px;
      height: auto;
      line-height: 20px;
      float: left;
      margin-top: 25px;
      div {
        img {
          width: 20px;
          height: 20px;
        }
      }
    }
  }
  .el-textarea__inner {
    min-height: 100px !important;
    border: none;
  }
  .el-upload--picture-card {
    width: 80px;
    height: 80px;
    line-height: 80px;
    margin-left: 20px;
  }
  .el-upload-list--picture-card .el-upload-list__item-thumbnail {
    width: 80px;
    height: 80px;
  }
  .el-upload-list--picture-card .el-upload-list__item {
    width: 80px;
    height: 80px;
    margin: 0 8px 8px 20px;
  }
  .el-upload--picture-card i {
    margin-top: 12px !important;
  }

  .toEvaluate .el-upload--picture-card i {
    margin-left: 4px !important;
  }
  .big_box {
    background: #f2f2f2;
    height: 755px;
    .service {
      background: #fff;
      float: left;
      width: 100%;
      margin-top: 10px;
      padding-bottom: 50px;

      .wuliu {
        text-align: left;
        padding-left: 20px;
        font-size: 18px;
      }
      .pj {
        padding-left: 20px;
        color: grey;
        font-size: 12px;
        text-align: left;
        display: block;
      }
      .star:first-child {
        margin-left: 50px;
      }
      .star {
        width: 30px;
        height: auto;
        line-height: 20px;
        float: left;
        margin-top: 15px;
        div {
          img {
            width: 20px;
            height: 20px;
          }
        }
      }
    }
  }
  .el-button--danger {
    width: 95%;
    margin-top: 7%;
  }
}
</style>
