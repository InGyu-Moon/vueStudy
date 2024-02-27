<template>

  <!-- <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Dongle&family=Gaegu&family=Nanum+Pen+Script&family=Noto+Sans+KR:wght@100..900&family=Noto+Serif+KR&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
  <script src="https://code.jquery.com/jquery-3.7.0.js"></script>
  <link href="https://fonts.googleapis.com/css2?family=Nanum+Pen+Script&display=swap" rel="stylesheet"> -->


  <div>
    <div class="menu">
      <!-- <a v-for="header in 3" :key="header">Home</a> -->
      <a  v-for="menu in menus" :key="menu">{{menu}}</a>
    </div>

    <!-- <div class="celeb">
      <img src="@/assets/images/1.jpg">
      <h3>{{ celeb[0] }}</h3>
      <p>소속사:하이브</p>
      <button @click="likes++">좋아요</button>
      <span>좋아요:{{ likes }}</span>
    </div>

    <div class="celeb">
      <img src="@/assets/images/5.jpg">
      <h3>{{ celeb[1] }}</h3>
      <p>소속사:SM</p>
    </div>

    <div class="celeb">
      <img src="@/assets/images/12.jpg">
      <h3>{{ celeb[2] }}</h3>
      <p>소속사:JYP</p>
    </div>

    <div class="celeb">
      <img src="@/assets/images/13.jpg">
      <h3>{{ celeb[2] }}</h3>
      <p>소속사:하이브</p>
    </div> -->
    
    <div class="celeb" v-for="(angency,key123) in angencys" :key="key123">
      <img :src="angency.imgSrc">
      <h3>{{ key123 }}. {{ angency.name }}</h3>
      <p>소속사: {{ angency.company }}</p>
      <button @click="onClickLikes(key123)">좋아요</button>
      <span>좋아요:{{ angency.likes }}</span>
    </div>






  </div>
</template>

<script>
export default {
  data () {
    return{
      menus:['Home','Celeb','About'],
      celeb:['여진구','최지우','박보영','박신혜','유아인'],
      angencys:[
        {name:'여진구',company:'하이브',likes:0,imgSrc:require('./assets/images/1.jpg')},
        {name:'최지우',company:'SM',likes:0,imgSrc:require('./assets/images/5.jpg')},
        {name:'박보영',company:'JYP',likes:0,imgSrc:require('./assets/images/12.jpg')},
        {name:'박신혜',company:'하이브',likes:0,imgSrc:require('./assets/images/13.jpg')},
        {name:'유아인',company:'SM',likes:0,imgSrc:require('./assets/images/20.jpg')}
      ],
    }
  },
  methods:{
    onClickLikes(num){
      this.angencys[num].likes++;
    }
  }
}
</script>

<style lang="css" scoped>
  .menu{
    background-color: blueviolet;
    padding: 10px;
    border-radius: 5px;
  }
  .menu a{
    color: white;
    margin: 10px

  }
  .celeb img{
    width: 150px;
    border-radius: 50px;
    margin-top: 30px;
  }
</style>