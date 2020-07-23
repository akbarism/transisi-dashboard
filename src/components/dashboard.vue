<template>
  <section class="dashboard">
    <nav>
      <div class="bars">
        <i class="fas fa-bars"></i>
      </div>
    </nav>
    <header>
      <h1>Hi Samantha</h1>
      <p>Welcomeback back to the workspae, we missed You!</p>
      <div class="search">
        <i class="fas fa-search lop"></i>
        <input type="text" placeholder="Search task Or Project.." />
      </div>
    </header>
    <div class="project">
      <section class="title">
        <h4>Projects</h4>
        <small>(13)</small>
      </section>
      <section class="card">
        <div class="item">
          <div class="outline">
            <div class="square-1">
              <h1>GH</h1>
            </div>
          </div>
          <p>Green House</p>
        </div>
        <div class="item">
          <div class="outline-2">
            <div class="square-2">
              <h1>CP</h1>
            </div>
          </div>
          <p>Cyber Punk</p>
        </div>
        <div class="item">
          <div class="outline">
            <div class="dot"></div>
            <div class="square-3">
              <h1>EC</h1>
            </div>
          </div>
          <p>Easy Crypto</p>
        </div>
        <div class="item">
          <div class="outline">
            <div class="square-4">
              <h1>TA</h1>
            </div>
          </div>
          <p>Travel App</p>
        </div>
        <div class="item">
          <div class="outline">
            <div class="dot"></div>
            <div class="square-5">
              <h1>LP</h1>
            </div>
          </div>
          <p>Landing Page</p>
        </div>
        <div class="item">
          <div class="outline">
            <div class="square-6">
              <h2>8+</h2>
            </div>
          </div>
        </div>
      </section>
    </div>
  </section>
</template>

<script>
export default {
  name: "dashboard"
};
</script>

<style lang="scss" scoped>
.dashboard {
  width: 50%;
  box-sizing: border-box;
  nav {
    color: #f8f8f8;
    margin-bottom: 100px;
    .bars {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 40px;
      height: 40px;
      border-radius: 10px;
      background: #3b3f54;
    }
  }
  header {
    box-sizing: border-box;
    height: 200px;
    margin-bottom: 20px;
    padding: 5px 100px;
    h1 {
      font-size: 50px;
      margin-bottom: 10px;
      color: #ffffff;
    }
    p {
      color: #898da2;
    }
    .search {
      position: relative;
      display: flex;
      align-items: center;
      color: #ffffff;
      margin-top: 20px;
      input {
        border: none;
        background: #3b3f54;
        width: 370px;
        height: 50px;
        border-radius: 10px;
        padding: 5px 0 5px 50px;
        box-sizing: border-box;
        color: #ffffff;
      }
      .lop {
        position: absolute;
        z-index: 2;
        margin-left: 20px;
      }
    }
  }
  .project {
    width: 100%;
    height: 300px;
    padding: 5px 100px;
    box-sizing: border-box;
    .title {
      display: flex;
      margin-bottom: 20px;
      h4 {
        color: #ffffff;
        margin-right: 10px;
      }
      small {
        color: #898da2;
      }
    }
    .card {
      display: flex;
      flex-wrap: wrap;
      width: 100%;
      box-sizing: border-box;
      .item {
        margin: 10px 15px 20px 0;
        text-align: center;
        .square-1 {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 100px;
          height: 100px;
          background: #e735c0;
          border-radius: 10px;
          color: #ffffff;
        }
        .outline-2 {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 110px;
          height: 110px;
          border: 3px solid #4792a4;
          border-radius: 10px;
          margin-top: -10px;
          margin-bottom: 15px;
        }
        .outline {
          position: relative;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: center;
          width: 113px;
          height: 113px;
        //   border: 3px solid #06070f;
          border-radius: 10px;
          margin-top: -10px;
          margin-bottom: 15px;
          .dot {
            top: -3px;
            right: -3px;
            position: absolute;
            width: 15px;
            height: 15px;
            background: #ffffff;
            border: 3px solid #06070f;
            border-radius: 50%;
          }
        }

        .square-2 {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 100px;
          height: 100px;
          background: #4180da;
          border-radius: 10px;
          color: #ffffff;
        }
        .square-3 {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 100px;
          height: 100px;
          background: #6f41bf;
          border-radius: 10px;
          color: #ffffff;
        }
        .square-4 {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 100px;
          height: 100px;
          background: #6e4cf0;
          border-radius: 10px;
          color: #ffffff;
        }
        .square-5 {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 100px;
          height: 100px;
          background: #ea7262;
          border-radius: 10px;
          color: #ffffff;
        }
        .square-6 {
          display: flex;
          justify-content: center;
          align-items: center;
          width: 100px;
          height: 100px;
          background: #3b3f54;
          border-radius: 10px;
          color: #ffffff;
        }
        p {
          color: #898da2;
        }
      }
    }
  }
}
@media only screen and (max-width: 768px) {
  .dashboard {
    width: 100%;
    height: 100%;
    margin-bottom: 250px;
    header {
        padding: 10px;
    }
    .project {
        padding: 10px;
        .card {
            justify-content: center;
            .item {
                margin: 10px;
            }
        }
    }
  }
}
</style>