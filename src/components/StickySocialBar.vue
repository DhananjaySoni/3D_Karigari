<template>
  <div class="social-share">
    <label class="toggle" for="toggle">
      <input type="checkbox" id="toggle" />
      <div class="btn">
        <i class="fas fa-share-alt mx-auto"></i>
        <i class="fas fa-times mx-auto"></i>
        <div class="social">
          <a href="#"><i class="fab fa-twitter"></i></a>
          <a href="#"><i class="fab fa-facebook-square"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fas fa-at"></i></a>
        </div>
      </div>
    </label>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.social-share {
  display: flex;
  flex-direction: row;
  position: fixed;
  bottom: 0;
  left:10px;
  z-index: 3;
}

.btn {
  height: 50px;
  width: 50px;
  border-radius: 50% !important;
  box-shadow: 4px 2px 10px 1px rgba(0, 0, 0, 0.2);
  display: flex;
  align-items: center !important;
  justify-content: center !important;
  font-size: 24px;
  color: rgb(116, 116, 116) !important;
  cursor: pointer;
  position: relative;
  background: #fff !important;
}
.btn .fa-share-alt {
  margin-right: 2px;

  height: 20px;
}
.btn .fa-times {
  margin-right: 2px;
  /* margin-top: 5px; */
  color: #e1306c;
}
.btn > i:hover {
  color: #405de6;
}
.btn:active:not(:focus-within) {
  box-shadow: -2px 2px 8px rgba(0, 0, 0, 0.2) inset;
}
.btn:active:not(:focus-within) > i {
  transform: translate(0.8px, 0.8px);
}

.social {
  box-shadow: 4px 2px 10px 1px rgba(0, 0, 0, 0.2);
  position: absolute;
  top: -90px;
  display: none;
  justify-content: space-between;
  background-color: white;
  /* padding: 17px 50px; */
  padding-top: 10px;
  padding-bottom: 10px;
  border-radius: 50px;
}
.toggle input[type="checkbox"]:checked + .btn .social {
  animation: fadeIn 1s;
  display: flex;
  flex-direction: column;
  /* margin-left: 300px; */
  margin-left: 150px;
  width: 80px;
  margin-top: -100px;
}
.toggle input[type="checkbox"]:not(:checked) + .btn .social {
  animation: fadeOut 1s;
}

.toggle input[type="checkbox"]:checked + .btn .fa-share-alt {
  display: none;
}
.toggle input[type="checkbox"]:not(:checked) + .btn .fa-times {
  display: none;
}
.social a {
  margin: 0 15px;
  font-size: 32px;
  color: #999;
}
.fa-twitter:hover{
    filter:drop-shadow(0px 0px 25px rgb(42, 166, 243));
}
.fa-facebook-square:hover{
    filter:drop-shadow(0px 0px 25px rgb(73, 161, 216));
}
.fa-instagram:hover{
    filter:drop-shadow(0px 0px 25px #e474c0);
}
.fa-at:hover{
    filter:drop-shadow(0px 0px 25px rgb(243, 146, 111));
}
.fa-twitter {
  color: rgb(29, 161, 242);
}
.fa-facebook-square {
  color: rgb(24, 130, 196);
}
.fa-instagram {
    color:white;
    height:30px;
    border-radius:8px;
    background: #d6249f;
    background: radial-gradient(circle at 30% 107%, #fdf497 0%, #fdf497 5%, #fd5949 45%,#d6249f 60%,#285AEB 90%);
    /* -webkit-background-clip: text; */
    -webkit-text-fill-color: transparent;
}
.fa-at {
  color: coral;
}

input[type="checkbox"] {
  display: none;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes fadeOut {
  from {
    opacity: 1;
  }
  to {
    opacity: 0;
  }
}
</style>
