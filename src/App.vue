<template>
  <h1>영화 정보</h1>
  <div v-for="(movie, i) in data" :key="i">
    <h3 class="bg-yellow" :style="textRed">{{ movie.title }}</h3>
    <p>개봉 : {{ movie.year }}</p>
    <p>장르 : {{ movie.category }}</p>
    <button @:click="increseLike(i)">좋아요</button> <span>{{ movie.like }}</span>
  </div>
  
</template>

<script>
  export default{
    name : 'App',
    data(){
      return {
        data: [
          {
            title:"노량",
            year: 2023,
            category: '액션, 드라마',
            textRed: "color : red",
            like: 0,
          },
          {
            title:"아쿠아맨과 로스트 킹덤",
            year: 2023,
            category: "액션, 판타지, 어드벤쳐",
            like: 0,
          },
          {
            title: "3월의 휴가",
            year:2023,
            category:"판타지, 드라마",
            like: 0,
          }
        ]
      }
    },
    methods:{
      increseLike(i){
        this.data[i].like += 1;
      }
    }
  }
</script>

<style>
  .bg-yellow{
    background-color: yellow;
    padding: 10px;
  }
</style>
