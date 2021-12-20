<template>
<div>
<div class="container">
  <div class="col-span-12 w-full">
    <div class="grid-col-12 w-full">
      <div class="col-span-12 sticky" style="background-color:green; height: 8vh; color:white; width: 100vw;">
          <div class="flex-row justify-between mx-0">
            <p>Name</p>
            <div>
              <p>link1</p>
              <p>link2</p>
              <p>link3</p>
            </div>
          </div>
        </div>
        <div class="col-span-12" style="background-color: black; height: 65vh; color: white;">
          <div class="flex-col justify-evenly h-max" style="margin-top: 8vh;">
            <p style="font-size: 8rem; margin-bottom: 0; margin-top: 0;">
              Art Vandelay
            </p>
            <div>
              <p style="font-size: 2rem; margin-bottom: 3vh; margin-top: 0;">
                Professional Photographer
              </p>
              <a  href="https://www.instagram.com/costanzagrams/" target="_blank">
                <button class="h-8vh w-12vw" style="background-color: transparent; color: white">
                  Learn More
                </button>
              </a>
            </div>
          </div>
        </div>
        <div class="col-span-12" style="background-color: blue; height: 100vh; color: white;">
        </div>
      </div>
    </div>
  <div class="col-span-12 w-full" style="background-color: red; height: 20rem; color: white;">
  </div>
  <div class="col-span-12 w-full" style="background-color: yellow; height: 6rem; color: white;">
  footer :)
  </div>
  </div>
</div>
</template>
<script>

export default {
  name: 'HomeRouter',
  props: {
    msg: String
  },
 data() {
  return {
    none: false,
  }
 },
 methods: {
   handleClick(tab, event) {
     console.log(tab, event);
   }
 }
}
</script>

<style lang="scss" scoped>

.sticky {
  position: fixed;
  top: 0;
  width: 100%;
}

/deep/ body {
  margin: 0 !important;
}

.container{
display: grid;
grid-template-columns: repeat(12, minmax(0, 1fr));
height: 100%;
width:100%;
margin:0;
justify-items: center;
overflow: hidden;
}
/deep/.el-tabs__header{
  margin: 0;
}
/deep/.el-tabs__nav {
  float:none;
}
/deep/.el-tabs__active-bar{
  visibility: hidden;
}

/deep/.el-tabs__nav-wrap {
  color:white;
  background-color: black;
  justify-items:center;
}

/deep/.el-tabs__item.is-active {
  position: relative;
  color: white;
}

// /deep/.el-tabs__item.is-active::after {
//   position: absolute;
//   content: '';
//   width: 4rem;
//   height: 0.1rem;
//   top:2rem;
//   right:0.8rem;
//   background-color: white;
//   transition: all .3s;
// }

/deep/.el-tabs__item {
  color: #b7b7b7;
}
</style>
