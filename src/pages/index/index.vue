<template>
  <view class="content">
    <view class="card personal-data">
      <view class="info">
        <view class="left">
          <view class="avatar">
            <text></text>
          </view>
          <view class="center">
            <view class="username">
              <text class="username-text">用户名用户名用户名</text>
            </view>
            <view class="level">
              <text>Lv. 16</text>
            </view>
          </view>
        </view>
        <view class="more">
          <button size="mini" plain="true" class="personal-more">
            查看详情
          </button>
        </view>
      </view>
      <view class="exp">
        <view class="data">
          <view class="exp-data">
            <text> exp: 1000/2000 </text>
          </view>
          <view class="gold-data">
            <text> $ 200 </text>
          </view>
        </view>
        <view class="exp-line">
          <view class="now"></view>
        </view>
      </view>
      <view class="attr-data">
        <view class="attr-item">心智：20</view>
        <view class="attr-item">体魄：20</view>
        <view class="attr-item">社交：20</view>
        <view class="attr-item">自律：20</view>
      </view>
    </view>
    <view class="task-category">
      <view class="task-category-item selected">
        <text class="task-category-item-text">编程学习编程</text>
      </view>
      <view class="task-category-item">
        <text class="task-category-item-text">学业任务</text>
      </view>
      <view class="task-category-item">
        <text class="task-category-item-text">每日任务</text>
      </view>
      <view class="task-category-item">
        <text class="task-category-item-text">健身目标</text>
      </view>
      <view class="task-category-item">
        <text class="task-category-item-text">更多</text>
      </view>
    </view>
    <view class="card task-data">
      <view class="task-item">
        <text class="task-item-text"
          >完成 Vue 3 学习完成 Vue 3 学习 完成 Vue 3 学习</text
        >
        <radio style="transform: scale(0.7)" borderColor="#aaa" />
      </view>
      <view class="task-item">
        <text class="task-item-text">完成 Vue 3 学习</text>
        <radio style="transform: scale(0.7)" borderColor="#aaa" />
      </view>
      <view class="task-item">
        <text class="task-item-text">完成 Vue 3 学习</text>
        <radio style="transform: scale(0.7)" borderColor="#aaa" />
      </view>
      <view class="more">
        <button size="mini" class="task-more">查看更多</button>
      </view>
    </view>
    <FloatPet />
  </view>
</template>

<script setup lang="ts">
import FloatPet from "@/components/FloatPet.vue/FloatPet.vue";
</script>

<style>
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding-bottom: 140rpx;
  height: 100vh;
  background-color: #fef8e6;
}

.card {
  background-color: #fff;
  width: 80vw;
  border-radius: 20rpx;
  box-shadow: 0 6rpx 10rpx #ccc;
  padding: 30rpx;
}

.personal-data {
  height: 35vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 50rpx;

  .info {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .left {
      display: flex;
      align-items: center;

      .avatar {
        width: 120rpx;
        height: 120rpx;
        background-color: #fe7a24;
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .center {
        margin-left: 20rpx;
        font-size: 36rpx;

        .username {
          .username-text {
            display: inline-block;
            overflow: hidden;
            text-overflow: ellipsis;
            white-space: nowrap;
            width: 30vw;
            vertical-align: middle;
          }
        }
      }
    }

    .personal-more {
      border: 2rpx solid #888;
      padding: 0 0.75em;
      display: flex;
      align-items: center;
    }
  }

  .exp {
    width: 100%;

    .data {
      width: 100%;
      display: flex;
      justify-content: space-between;
      margin-bottom: 10rpx;
      font-size: 28rpx;
    }

    .exp-line {
      width: 100%;
      background-color: #e2ecf8;
      height: 20rpx;
      border-radius: 10rpx;
      box-shadow: 0 2rpx 5rpx #ccc;

      .now {
        width: 50%;
        height: 100%;
        background-color: #fe7a24;
        border-radius: 10rpx;
      }
    }
  }

  .attr-data {
    width: 100%;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10rpx;

    .attr-item {
      font-size: 28rpx;
      width: 47%;
      padding: 10rpx;
      /* border: 1px solid #ddd; */
    }
  }
}

.task-category {
  width: 80vw;
  display: flex;
  align-items: center;
  justify-content: space-between;
  overflow: auto;
  gap: 15rpx;

  .task-category-item {
    border-radius: 20rpx;
    background-color: #fcfcfc;
    border-radius: 20rpx;
    font-size: 28rpx;
    box-shadow: 0 6rpx 10rpx #ccc;
    padding: 20rpx;
  }

  .task-category-item-text {
    white-space: nowrap;
  }

  .selected {
    background-color: #fe7a24;
    color: #fff;
  }

  .more {
    background-color: #d0d0d0;
  }
}

.task-data {
  margin-top: 20rpx;
  height: 35vh;
  box-shadow: inset 0 0 0 10rpx #fe7a24cc;

  .task-item {
    padding: 20rpx;
    border-bottom: 2rpx solid #ddd;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;

    .task-item-text {
      line-height: 1.5;
      white-space: nowrap;
      width: 85%;
      overflow: hidden;
      text-overflow: ellipsis;
      vertical-align: middle;

      &::before {
        content: " ";
        display: inline-block;
        width: 10rpx;
        height: 28rpx;
        background-color: #fe7a24;
        margin-right: 20rpx;
      }
    }
  }
  .more {
    margin-top: 30rpx;
    text-align: center;
    font-size: 28rpx;
    .task-more {
      background-color: #fe7a24;
      color: #fff;
      border-radius: 20rpx;
      font-size: 28rpx;
    }
  }
}
</style>
