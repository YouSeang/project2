<template>
  <div class="container" style="margin-top: 70px;">
    <h2>{{ $route.params.title }}</h2>
    <p>{{ $route.params.content }}</p>
    <p class="text-muted">{{ $route.params.sendtime }}</p>
    <hr class="my-4">
    <div class="button-wrap">
      <button @click="fnList" class="btn cancel">목록</button>
      <button class="btn edit">수정</button>
      <button class="btn delete">삭제</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: [],
      memberNo: 1,
    };
  },
  methods: {
    fnList() { // 리스트 화면으로 이동
      this.$router.push('/story');
    },
  }
};
</script>

<style scoped>
.container {
  width: 100%;
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  background-color: #fff;
  border-radius: 5px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}

h2 {
  color: #43b984;
  font-size: 24px;
  margin-bottom: 10px;
}

p {
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 10px;
}

.text-muted {
  color: #888;
}

hr {
  border: none;
  border-top: 1px solid #ccc;
  margin: 20px 0;
}

.button-wrap {
  text-align: right;
}

.button-wrap .btn {
  padding: 10px 20px;
  margin-left: 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}

.button-wrap .btn.cancel {
  background-color: #ccc;
  color: #333;
}

.button-wrap .btn.edit {
  background-color: #f0ad4e;
  color: #fff;
}

.button-wrap .btn.delete {
  background-color: #d9534f;
  color: #fff;
}
</style>0.0



.
