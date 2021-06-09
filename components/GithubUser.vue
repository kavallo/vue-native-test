<template>
  <view class="github-user">
    <image class="github-user__image" :source="{ uri: user.avatar_url }" />
    <text>{{ user.login }}</text>
    <text>{{ user.contributions }} contributions</text>
  </view>
</template>

<script>
export default {
  props: {
    user: Object,
  },
};
</script>
<style>
.github-user {
  padding: 16px;
  align-items: center;
}

.github-user__image {
  width: 50px;
  height: 50px;
  border-radius: 25px;
  margin-bottom: 5px;
}
</style>