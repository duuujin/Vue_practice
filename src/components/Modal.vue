<template>
  <div class="modal" v-if="isModal">
    <div class="modal-inner">
      <!-- 닫기 버튼 -->
      <button class="close-btn" @click="$emit('closeModal')">✕</button>

      <!-- 영화 이미지 -->
      <div class="poster">
        <img :src="data[selectedMovie].imgUrl" :alt="data[selectedMovie].title" />
      </div>

      <!-- 영화 정보 -->
      <div class="info">
        <h1>{{ data[selectedMovie].title }}</h1>
        <p class="like">❤️ {{ data[selectedMovie].like }}</p>
        <p class="story">{{ data[selectedMovie].story }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ModalComponent",
  props: {
    data: Array,
    isModal: Boolean,
    selectedMovie: Number,
  }
}
</script>

<style>
.modal {
  position: fixed;
  inset: 0; /* top:0; left:0; right:0; bottom:0; */
  background-color: rgba(0,0,0,0.85);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 999;
  overflow-y: auto;
  padding: 20px;
}

.modal-inner {
  position: relative;
  display: flex;
  flex-direction: row;
  max-width: 900px;
  width: 90%;
  background-color: #141414; /* 넷플릭스 다크톤 */
  border-radius: 12px;
  overflow: hidden;
  color: #fff;
  box-shadow: 0 0 40px rgba(0,0,0,0.8);
}

.close-btn {
  position: absolute;
  top: 15px;
  right: 15px;
  background: rgba(0,0,0,0.7);
  color: #fff;
  border: none;
  border-radius: 50%;
  width: 35px;
  height: 35px;
  font-size: 18px;
  cursor: pointer;
}

.poster {
  flex: 1;
  min-width: 300px;
  background: linear-gradient(to bottom, transparent, #141414);
}

.poster img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.info {
  flex: 1.5;
  padding: 20px;
  flex-direction: column;
  justify-content: flex-start;
}

.info h1 {
  font-size: 2rem;
  margin-bottom: 15px;
} */

.info .like {
  font-size: 1.2rem;
  margin-bottom: 15px;
}

.info .story {
  font-size: 1rem;
  line-height: 1.5;
}
</style>
