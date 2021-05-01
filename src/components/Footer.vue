<template>
  <div class="footer">
    <div class="footer_container row">
      <div class="footer_left col-6 col-sm-4">
        <p>2021 &copy; 3D&nbsp;Karigari</p>
      </div>
      <div class="footer_mid col-6 col-sm-4">
        <img src="/img/makeinindia.png" alt="#makeinindia" />
      </div>
      <div class="footer_right col-12 col-sm-4">
        <ul class="social_links">
          <li>
            <a
              target="blank"
              rel="noopener noreferrer"
              href="https://www.instagram.com/"
              ><b-icon icon="instagram"></b-icon
            ></a>
          </li>
          <li>
            <a
              target="blank"
              rel="noopener noreferrer"
              href="https://twitter.com/"
              ><b-icon icon="twitter"></b-icon
            ></a>
          </li>
          <li>
            <a
              target="blank"
              rel="noopener noreferrer"
              href="https://api.whatsapp.com/send?phone=+91XXXX"
              ><b-icon icon="instagram"></b-icon
            ></a>
          </li>
          <li>
            <a
              target="blank"
              rel="noopener noreferrer"
              href="mailto:someone@example.com"
              ><b-icon icon="envelope"></b-icon
            ></a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.footer {
  background: #757575;
  width: 100%;
  height: 8vh;
  z-index: 1;
  padding: 0;
  position: absolute;
  bottom: 0;
  left: 0;
}

.footer_container {
  display: flex;
  align-items: center;
  height: 100%;
  margin: auto;
}

.row {
  height: 100%;
  margin: auto;
  padding: 0;
}

.footer div {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;
  text-align: center;
}

div.footer_left p {
  color: rgb(255, 255, 255);
  margin: 0;
  font-size: 90%;
}

div.footer_mid img {
  height: 40px;
}

ul.social_links {
  list-style: none;
  display: flex;
  justify-content: space-evenly;
  width: 100%;
  align-items: center;
  margin: 0;
  padding: 0;
}

.social_links svg {
  color: #444;
}

ul li a {
  text-decoration: none;
}

.social_links li:nth-child(1) a svg {
  color: pink;
}

.social_links li:nth-child(2) a svg {
  color: #00aced;
}

.social_links li:nth-child(3) a svg {
  color: lightgreen;
}

.social_links li:nth-child(4) a svg {
  color: white;
}

@media screen and (max-width: 576px) {
  div.footer_mid img {
    height: 30px;
  }
  div.footer_left p {
    font-size: 80%;
  }
}
</style>