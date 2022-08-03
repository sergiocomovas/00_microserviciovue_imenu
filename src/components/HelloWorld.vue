<!--<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>-->

<script>
export default {
  props: ["msg"],
  created() {
    // props are exposed on `this`
    console.log(this.foo);
  },
};
</script>

<template>
  <div class="xnav">
    <input type="checkbox" >
    <span></span>
    <span></span>
    <span></span>
    <div class="xmenu">
      <li><a href="#">home</a></li>
      <li><a href="#">about</a></li>
    </div>
  </div>
</template>

<style scoped>
.xnav,
.xmenu {
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: "Arial", "Open Sans", Verdana, Geneva, Tahoma, sans-serif;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.xnav {
  position: fixed;
  bottom:15px;
  right:15px;
  background-color: #fff;
  padding: 20px;
  transition: 0.5s;
  border-radius: 50px;
  overflow: hidden;
  box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
}

.xmenu {
  margin: 0;
  padding: 0;
  width: 0;
  overflow: hidden;
  transition: 0.5s;
}

.xnav input:checked ~ .xmenu {
  width: 450px;
}

.xmenu li {
  list-style: none;
  margin: 0 10px;
}

.xmenu li a {
  text-decoration: none;
  color: #666;
  text-transform: uppercase;
  font-weight: 600;
  transition: 0.5s;
}

.xmenu li a:hover {
  color: #161919;
}

.xnav input {
  width: 40px;
  height: 40px;
  cursor: pointer;
  opacity: 0;
}

.xnav span {
  position: absolute;
  left: 30px;
  width: 30px;
  height: 4px;
  border-radius: 50px;
  background-color: #666;
  pointer-events: none;
  transition: 0.5s;
}

.xnav input:checked ~ span {
  background-color: #f974a1;
}

.xnav span:nth-child(2) {
  transform: translateY(-8px);
}

.xnav input:checked ~ span:nth-child(2) {
  transform: translateY(0) rotate(-45deg);
}
.xnav span:nth-child(3) {
  transform: translateY(8px);
}

.xnav input:checked ~ span:nth-child(3) {
  transform: translateY(0) rotate(45deg);
}

.xnav input:checked ~ span:nth-child(4) {
  transform: translateY(0) rotate(45deg);
}
</style>
