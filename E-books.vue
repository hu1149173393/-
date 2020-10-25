<template>
  <div class="E_books">
    <div>
      <ul >
        <li class="e-book">
          <p class="mybook"><Icon type="md-book" />技术</p>
          <p class="book"></p>
          <p class="book"></p>
          <p class="book"></p>
          <p class="book"></p>
        </li>
        <li class="e-book">
          <p class="mybook"><Icon type="md-book" />古文</p>
          <p class="book"></p>
          <p class="book"></p>
          <p class="book"></p>
          <p class="book"></p>
        </li>
        <li class="e-book">
          <p class="mybook"><Icon type="md-book" />漫画</p>
          <p class="book"></p>
          <p class="book"></p>
          <p class="book"></p>
          <p class="book"></p>
        </li>
        <li class="e-book">
          <p class="mybook"><Icon type="md-book" />科技</p>
          <p class="book"></p>
          <p class="book"></p>
          <p class="book"></p>
          <p class="book"></p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
    name:'E_books'
}
</script>

<style>

ul li{
  list-style: none;
}
.E_books{
  width: 100%;
  height: 100%;
  /* border: 1px solid red; */
}
.e-book{
  display: flex;
  justify-content: space-around;
  margin: 10px 0 10px 0;
}
.mybook{
  width: 70px;
  height: 40px;
  line-height: 20px;
  padding: 10px;
  margin: 10px 0 10px 0;
  background-color: rgba(0, 0, 0, 0.1);
  border: 1px solid orange;
  border-top-left-radius: 50%;
  border-bottom-right-radius: 50%;
}
.book{
  width: 200px;
  height: 230px;

  background-color: rgba(0, 0, 0, 0.15);
}
</style>