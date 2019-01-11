<template>
  <div class="card">
    <div class="image-section">
        <p>
          <img :src="chara.image">
        </p>
    </div>
    <div class="card-section">
      <h1>{{ chara.name }}</h1>
      <p class="title">{{ chara.title }}</p>
      <div class="content">
          <h3>Inspiration</h3>
          <p class="text">
              <span v-if="chara.inspiration[0]">1st</span>
              <span v-if="chara.inspiration[1]">2nd</span>
          </p>
          <h3>Condition</h3>
          <p class="text">under construction</p>
      </div>
      <div class="link">
          <p><a :href="chara.sheet" target="_blank">Open Character Sheet</a></p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: {
      chara: Object
    }
  };
</script>

<style lang="scss" scoped>
  .card{
    display: flex;
    flex-wrap: nowrap;
    justify-content:flex-start;
  }
  .image-section{
    box-shadow: 0 2px 5px #8c7b75;
    border-radius: 5px 0 0 5px;
    width: 120px;
    p{
      margin: 0;
      height: 100%;
      border-radius: 5px 0 0 5px;
      background: #8c7b75;
      position: relative;
    }
    img{
      display: block;
      opacity: 0.2;
      border-radius: 5px 0 0 5px;
      width: 100%;
      height: 100%;
      position: absolute;
      bottom: 0;
      right: 0;
    }
  }
  .card-section{
    padding: 1rem;
    padding-top: 0.1rem;
    padding-bottom: 0.5rem;
    border-radius: 0 5px 5px 0;
    box-shadow: 0 2px 5px #8c7b75;
    width: 500px;
    height: 100%;
    background:#efdcd5;

    h1{
      font-size: 20px;
      margin-top: 0.5rem;
      margin-bottom: 0.01rem;
      padding-bottom: 0.01rem;
      text-align: right;
    }

    .title{
      margin-top: .1rem;
      font-size:14px;
      color: #555;
      text-align: right;
      border-bottom: 2px solid #333;
    }

    h3{
      font-size: 15px;
      color: #222;
      margin-bottom: 0.2rem;
      border-bottom: 1px solid #000;

    }

    .text{
      margin-top: 0.2rem;
      margin-bottom: 1rem;
    }

    .content{
      margin-top: 1rem;
    }
    .link{
      margin-left: -1rem;
      margin-right: -1rem;
      padding-left: 1rem;
      padding-right: 1rem;
      border-top: 1px solid #ccc;
      text-align: right;
      p{
        margin: 0;
        margin-top: 0.5rem;
        font-size: 13px;
      }
    }
  }
</style>