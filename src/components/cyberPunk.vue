<template>
  <header>
    <section class="sub-menu">
      <h1>Cyber Punk</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt.</p>
    </section>
    <section class="member">
      <div class="img-group">
        <img src="../assets/img/user-4.jpg" alt="user" />
        <img src="../assets/img/user-5.jpg" alt="user" />
        <img src="../assets/img/user-gr.jpg" alt="user" />
      </div>
      <div class="plus">
        <i class="fas fa-plus"></i>
      </div>
    </section>
  </header>
</template>

<script>
export default {
    name: "cyberpunk"
};
</script>

<style lang="scss" scoped>
    header {
      display: flex;
      padding: 50px 70px 20px 70px;
      box-sizing: border-box;
      .sub-menu {
        width: 60%;
        h1 {
          font-size: 30px;
          margin-bottom: 20px;
          font-weight: 700;
        }
        p {
          color: #898da2;
          font-size: 13px;
          font-weight: 600;
        }
      }
      .member {
        display: flex;
        justify-content: flex-end;
        width: 40%;
        .img-group {
          display: flex;
          flex-direction: row-reverse;
          position: relative;
          margin-right: 20px;
          img {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: 3px solid #ffffff;
            margin-right: -10px;
          }
        }
        .plus {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 25px;
          height: 25px;
          background: #ffffff;
          border: 3px solid #d3d3d3;
          color: #d3d3d3;
          border-radius: 50%;
          margin-top: 7px;
          cursor: pointer;
        }
      }
    }
    @media only screen and (max-width: 768px) {
        header {
            flex-direction: column;
            .sub-menu {
                width: 100%;
                margin-bottom: 20px;
            }
            .member {
                width: 100%;
                justify-content: center;
            }
        }
    }
</style>