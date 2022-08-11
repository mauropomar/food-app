<template>
  <div class="home">
    <div class="header">
      <h2 class="title">Hi <b>Vadim!</b></h2>
      <div class="input">
        <input type="text" placeholder="Find what you want..." />
        <div class="icon-input">
          <i class="bx bx-search"></i>
        </div>
      </div>
      <div class="combo-header">
        <div class="text">
          <h3>Free combo</h3>
          <p>Burger + Coca cola for new users</p>
        </div>
        <div class="img">
          <img
            src="https://image.shutterstock.com/image-photo/fresh-homemade-italian-pizza-margherita-600w-1829205563.jpg"
            alt=""
          />
        </div>
      </div>
    </div>
    <div class="scroll-header">

    </div>
  </div>
</template>

<style lang="less">
.home {
  margin: 20px;
}
.header {
  .combo-header {
    background-color: rgba(74, 174, 84);
    color: white;
    padding: 20px;
    border-radius: 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top:20px;
    .img {
      width: 50%;
      img {
        object-fit: cover;
        border-radius: 10px;
        width: 100%;
      }
    }
    .text {
      width: 50%;
      h3 {
        font-weight: 400;
      }
      p {
        font-weight: 300;
      }
    }
  }
  .input {
    display: flex;
    align-items: center;
    position: relative;
    margin-top: 15px;
    input {
      width: 100%;
      background-color: rgba(250, 248, 248);
      border: 0px;
      outline: none;
      padding: 10px;
      padding-left: 30px;
      border-radius: 10px;
    }
    .incon-input {
      position: absolute;
      margin-left: 10px;
    }
  }
  .title {
    font-weight: 350;
  }
}
</style>
