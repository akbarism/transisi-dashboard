<template>
  <div class="home">
    <Dashboard />
    <section class="main-menu">
      <Cyberpunk />
      <Today />
      <section class="upcoming">
        <div class="child-menu">
          <h4>Upcoming</h4>
          <i class="fas fa-ellipsis-h dot"></i>
        </div>
        <div class="list">
          <section class="list-item">
            <div class="todos">
              <label class="checkbox-label">
                <input type="checkbox" />
                <span class="checkbox-custom circular"></span>
              </label>
              <h4>Create initial layout for homepage</h4>
            </div>
            <div class="Waiting">
              <p>Waiting</p>
            </div>
          </section>
          <section class="list-item">
            <div class="todos">
              <label class="checkbox-label">
                <input type="checkbox" />
                <span class="checkbox-custom circular"></span>
              </label>
              <h4>Discussions regarding workflow improvement</h4>
            </div>
            <div class="Waiting">
              <p>Waiting</p>
            </div>
          </section>
          <section class="list-item">
            <div class="todos">
              <label class="checkbox-label">
                <input type="checkbox" />
                <span class="checkbox-custom circular"></span>
              </label>
              <h4>Fixing icons with transpaarant background</h4>
            </div>
            <div class="Waiting">
              <p>Waiting</p>
            </div>
          </section>
          <section class="list-item" v-for="list in temp" :key="list.id">
            <div class="todos">
              <label class="checkbox-label">
                <input type="checkbox" :checked="list.checked" />
                <span class="checkbox-custom circular"></span>
              </label>
              <h4>{{list.title}}</h4>
            </div>
            <div :class="list.status">
              <p>{{list.status}}</p>
            </div>
          </section>
        </div>
      </section>
      <footer>
        <button class="btn-plus" @click="random">
          <i class="fas fa-plus"></i>
        </button>
      </footer>
    </section>
  </div>
</template>

<script>
import Dashboard from "../components/dashboard.vue";
import Cyberpunk from "../components/cyberPunk.vue";
import Today from "../components/today.vue";
export default {
  name: "Home",
  components: {
    Dashboard,
    Cyberpunk,
    Today
  },
  data() {
    return {
      lists: [
        {
          checked: false,
          title: "Fixing icons with transpaarant background",
          status: "Waiting"
        },
        {
          checked: false,
          title: "Discussions regarding workflow improvement",
          status: "Approved"
        },
        {
          checked: true,
          title: "Create initial layout for homepage",
          status: "Waiting"
        }
      ],
      temp: []
    };
  },
  methods: {
    random() {
      const item = this.lists[Math.floor(Math.random() * this.lists.length)];
      this.temp.push(item);
    }
  }
};
</script>

<style lang="scss" scoped>
.home {
  display: flex;
  width: 100%;
  padding: 15px;
  background: #06070f;
  box-sizing: border-box;
  .main-menu {
    width: 50%;
    background: #ffffff;
    border-radius: 10px;
    .upcoming {
      width: 100%;
      padding: 10px 70px;
      box-sizing: border-box;
      margin-top: 20px;
      .child-menu {
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 2px solid #f7f7f7;
        width: 100%;
        height: 45px;
        margin-bottom: 15px;
        .dot {
          color: #eceef0;
        }
      }
      .list {
        display: flex;
        flex-direction: column;
        height: 150px;
        overflow-y: scroll;
        .list-item {
          display: flex;
          justify-content: space-between;
          margin: 10px 0;
          .todos {
            display: flex;
            align-items: center;
            color: #bbbec5;
            font-size: 14px;
            h4 {
              margin-left: 20px;
            }
          }
          .Approved {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100px;
            background: #e0f5f5;
            border-radius: 10px;
            padding: 5px 0;
            p {
              font-size: 10px;
              font-weight: 600;
              color: #73c4c4;
            }
          }
          .Waiting {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100px;
            background: #e0f5f5;
            border-radius: 10px;
            padding: 5px 0;
            p {
              font-size: 10px;
              font-weight: 600;
              color: #cacfd4;
            }
          }
        }
      }
    }
    footer {
      display: flex;
      justify-content: flex-end;
      margin-top: 30px;
      width: 100%;
      padding: 10px 30px;
      box-sizing: border-box;
      button {
        height: 50px;
        width: 50px;
        border-radius: 10px;
        border: none;
        background: #884ec6;
        color: #ffffff;
        font-size: 20px;
        box-shadow: 0px 17px 29px 0px rgba(136, 78, 198, 0.41);
      }
    }
  }
}
.checkbox-label {
  /* display: block; */
  position: relative;
  cursor: pointer;
  font-size: 22px;
  line-height: 24px;
  height: 20px;
  width: 20px;
  clear: both;
}

.checkbox-label input {
  /* position: absolute; */
  opacity: 0;
  cursor: pointer;
}

.checkbox-label .checkbox-custom {
  position: absolute;
  top: 0px;
  left: 0px;
  height: 20px;
  width: 20px;
  background-color: transparent;
  border-radius: 5px;
  transition: all 0.3s ease-out;
  -webkit-transition: all 0.3s ease-out;
  -moz-transition: all 0.3s ease-out;
  -ms-transition: all 0.3s ease-out;
  -o-transition: all 0.3s ease-out;
  border: 2px solid #f7f7f7;
}

.checkbox-label .checkbox-custom::after {
  position: absolute;
  content: "";
  left: 12px;
  top: 12px;
  height: 0px;
  width: 0px;
  border-radius: 5px;
  border: solid #ffffff;
  border-width: 0 3px 3px 0;
  -webkit-transform: rotate(0deg) scale(0);
  -ms-transform: rotate(0deg) scale(0);
  transform: rotate(0deg) scale(0);
  opacity: 1;
  transition: all 0.3s ease-out;
  -webkit-transition: all 0.3s ease-out;
  -moz-transition: all 0.3s ease-out;
  -ms-transition: all 0.3s ease-out;
  -o-transition: all 0.3s ease-out;
}

.checkbox-label input:checked ~ .checkbox-custom::after {
  -webkit-transform: rotate(45deg) scale(1);
  -ms-transform: rotate(45deg) scale(1);
  transform: rotate(45deg) scale(1);
  opacity: 1;
  left: 7px;
  top: 4px;
  width: 4px;
  height: 9px;
  border: solid #ffffff;
  border-width: 0 2px 2px 0;
  background-color: transparent;
  border-radius: 0;
}

/* For Ripple Effect */
.checkbox-label .checkbox-custom::before {
  position: absolute;
  content: "";
  left: 10px;
  top: 10px;
  width: 0px;
  height: 0px;
  border-radius: 5px;
  border: 2px solid #f7f7f7;
  -webkit-transform: scale(0);
  -ms-transform: scale(0);
  transform: scale(0);
}

.checkbox-label input:checked ~ .checkbox-custom::before {
  left: -3px;
  top: -3px;
  width: 20px;
  height: 20px;
  border-radius: 5px;
  -webkit-transform: scale(3);
  -ms-transform: scale(3);
  transform: scale(3);
  opacity: 0;
  z-index: 999;
  transition: all 0.3s ease-out;
  -webkit-transition: all 0.3s ease-out;
  -moz-transition: all 0.3s ease-out;
  -ms-transition: all 0.3s ease-out;
  -o-transition: all 0.3s ease-out;
}

/* Style for Circular Checkbox */
.checkbox-label .checkbox-custom.circular {
  border-radius: 50%;
  border: 2px solid #e6e3e3;
}

.checkbox-label input:checked ~ .checkbox-custom.circular {
  background-color: #6bd9d8;
  border-radius: 50%;
  border: 2px solid #6bd9d8;
}
.checkbox-label input:checked ~ .checkbox-custom.circular::after {
  border: solid #ffffff;
  border-width: 0 2px 2px 0;
}
.checkbox-label .checkbox-custom.circular::after {
  border-radius: 50%;
}

.checkbox-label .checkbox-custom.circular::before {
  border-radius: 50%;
  border: 2px solid #6bd9d8;
}

.checkbox-label input:checked ~ .checkbox-custom.circular::before {
  border-radius: 50%;
}
::-webkit-scrollbar {
  width: 5px;
}
/* Track */
::-webkit-scrollbar-track {
  background: #ffffff;
}
/* Handle */
::-webkit-scrollbar-thumb {
  /* background: #888;  */
  background: #cacfd4;
}
/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  /* background: #555;  */
  background: #e1e3e6;
}
@media only screen and (max-width: 768px) {
  .home {
    flex-direction: column;
    align-items: center;
    height: 100%;
    .main-menu {
      width: 100%;
      .upcoming {
        padding: 15px;
      }
    }
  }
}
</style>
