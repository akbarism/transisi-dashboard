<template>
  <section class="today">
    <div class="child-menu">
      <h4>Today</h4>
      <i class="fas fa-ellipsis-h dot"></i>
    </div>
    <div class="list">
      <section class="list-item">
        <div class="todos">
          <label class="checkbox-label">
            <input type="checkbox" checked="true" />
            <span class="checkbox-custom circular"></span>
          </label>
          <h4>Create initial layout for homepage</h4>
        </div>
        <div class="aproved">
          <p>Approved</p>
        </div>
      </section>
      <section class="list-item">
        <div class="todos">
          <label class="checkbox-label">
            <input type="checkbox" checked="true" />
            <span class="checkbox-custom circular"></span>
          </label>
          <h4>Fixing icons with transpaarant background</h4>
        </div>
        <div class="progres">
          <p>In Progress</p>
        </div>
      </section>
      <section class="list-item">
        <div class="todos">
          <label class="checkbox-label">
            <input type="checkbox" checked="true" />
            <span class="checkbox-custom circular"></span>
          </label>
          <h4>Fixing icons with transpaarant background</h4>
        </div>
        <div class="progres">
          <p>In Progress</p>
        </div>
      </section>
      <section class="list-item">
        <div class="todos">
          <label class="checkbox-label">
            <input type="checkbox" checked="true" />
            <span class="checkbox-custom circular"></span>
          </label>
          <h4>Create initial layout for homepage</h4>
        </div>
        <div class="progres">
          <p>In Progress</p>
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
        <div class="review">
          <p>In Review</p>
        </div>
      </section>
      <section class="list-item">
        <div class="todos">
          <label class="checkbox-label">
            <input type="checkbox" />
            <span class="checkbox-custom circular"></span>
          </label>
          <h4>Create quotation for app redesign project</h4>
        </div>
        <div class="waiting">
          <p>Waiting</p>
        </div>
      </section>
    </div>
  </section>
</template>

<script>
export default {
  name: "Today"
};
</script>

<style lang="scss" scoped>
.today {
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
      .aproved {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100px;
        background: #e0f5f5;
        border-radius: 10px;
        padding: 3px;
        p {
          font-size: 10px;
          font-weight: 600;
          color: #73c4c4;
        }
      }
      .progres {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100px;
        background: #e4effe;
        border-radius: 10px;
        padding: 5px 0;
        p {
          font-size: 10px;
          font-weight: 600;
          color: #a4c3e3;
        }
      }
      .review {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100px;
        background: #fbeee8;
        border-radius: 10px;
        padding: 5px 0;
        p {
          font-size: 10px;
          font-weight: 600;
          color: #d9ad9c;
        }
      }
      .waiting {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100px;
        background: #eceef0;
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
@media only screen and (max-width: 768px) {
  .today {
    padding: 15px;
  }
}
</style>