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
    <div class="scroll-menu">
      <div class="scroll-content">
        <div :key="index" class="avatar" v-for="(item, index) in avatars">
          <i :class="item"></i>
        </div>
      </div>
    </div>
    <h2>Top Products</h2>
    <div class="scroll-menu">
      <div class="scroll-content">
        <div :key="index" v-for="(item, index) in products">
          <div class="top-products">
            <div class="top-products-img">
              <img
                :src="item.src"
                :alt="item.alt"
              />
            </div>
            <div class="top-products-text">
              <div class="top-products-title">{{item.title}}</div>
              <div class="top-products-price">{{item.price}}</div>
            </div>
            <i class="bx bx-plus-medical"></i>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
  data() {
    return {
      avatars: [
        "bx bxs-pizza bx-sm",
        "bx bxs-bowl-hot bx-sm",
        "bx bxs-baguette bx-sm",
        "bx bxs-drink bx-sm",
        "bx bxs-beer bx-sm",
        "bx bxs-wine bx-sm",
      ],
      products:[{
        title:'Berry Juice',
        price:'$7.5',
        src:'https://images.unsplash.com/photo-1551782450-a2132b4ba21d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1169&q=80',
        alt:'Hamburguesa'
      },{
        title:'Pizza',
        price:'$9.5',
        src:'https://media.istockphoto.com/id/1349383878/nl/foto/hawaiian-pizza-with-ham-and-pineapple.webp?s=612x612&w=is&k=20&c=zDYihZaHj_HAIaNTkS0jkKOccjgtUzSUBEYBTm0Nw94=',
        alt:'Pizza'
      },{
        title:'Drink',
        price:'$17.5',
        src:'https://images.unsplash.com/photo-1623934397237-ce68cb0285b3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8MzF8fGRyaW5rfGVufDB8fDB8fA%3D%3D&auto=format&fit=crop&w=400&q=60',
        alt:'drink'
      },{
        title:'Wine',
        price:'$3.5',
        src:'https://images.unsplash.com/photo-1510812431401-41d2bd2722f3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80',
        alt:'Wine'
      },{
        title:'Fish',
        price:'$88.9',
        src:'https://images.unsplash.com/photo-1519708227418-c8fd9a32b7a2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80',
        alt:'Fish'
      },{
        title:'Chicken',
        price:'$4.5',
        src:'https://images.unsplash.com/photo-1574672280600-4accfa5b6f98?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1170&q=80',
        alt:'Chicken'
      }]
    };
  },
};
</script>

<style lang="less">
.home {
  margin: 20px;
  .top-products {
    position: relative;
    min-width: 110px;
    padding: 10px;
    border-radius: 10px;
    background-color: rgba(250, 248, 248);
    .top-products-img {
      img {
        width: 100%;
      }
    }
    i {
      position: absolute;
      right: 0;
      bottom: 0;
      padding: 10px;
      color: white;
      border-radius: 50px;
      background-color: rgba(74, 174, 84);
      margin: 5px;
    }
    .top-products-text {
      margin-top: 10px;
      .top-products-price {
        font-weight: bold;
        font-size: 9px;
        color: rgba(255, 131, 84);
      }
      .top-products-title {
        font-weight: bold;
        font-size: 11px;
        color: rgba(47, 47, 47);
      }
    }
  }
  .scroll-menu {
    .scroll-content {
      display: flex;
      overflow-y: auto;
      .avatar {
        background-color: rgba(250, 248, 248);
        padding: 20px;
        border-radius: 10px;
        i {
          color: rgba(255, 131, 62);
        }
      }
    }
  }
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
    margin-top: 20px;
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
