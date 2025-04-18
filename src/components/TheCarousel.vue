<template>
  <el-carousel indicator-position="outside">
    <el-carousel-item v-for="(item, index) in items" :key="index">
      <div class="carousel-content">
        {{ item }}
      </div>
    </el-carousel-item>
  </el-carousel>
</template>

<script>
export default {
  data() {
    return {
      items: [
        "Fayl1.txt",
        "Fayl2.pdf",
        "Fayl3.docx",
      ], // Fayl nomlarini shu yerga qo'shing
    };
  },
};
</script>

<style scoped>
.carousel-content {
  font-size: 20px;
  text-align: center;
  padding: 20px;
  color: #333;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>
