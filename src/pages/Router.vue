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
        <div class="col-span-12" style="background-color: white; height: 60vh; color: white;">
          <div class="flex-col justify-evenly h-max">
            <div class="flex-row w-max justify-center">
                <img :src="art" class="h-40vh w-18vw mx-auto" style="object-fit: cover;"/>
              <div class="h-40vh w-40vw mx-auto" style="background-color:yellow;">
                <div class="flex-col">
                  <p style="color:white;">
                  Hey I'm Art!
                  </p>
                  <p style="color:white;">
                  I've always had an eye for design. I was a long time importer/exporter of goggles and long matchsticks, one day
                  a shipping mistake meant that I imported cameras instead of matchsticks and the rest is history. I am available to
                  photograph weddings, birthdays, special events and Festivus celebrations.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  <div class="col-span-12 w-full" style="background-color: white; height: auto; color: white;">
  <div class="flex-col justify-around h-max">
            <div class="wrap-content-screen-size w-max justify-between flex-wrap">
              <img :src="tree1" class="h-60vh w-auto mx-auto" style="object-fit: cover; margin-bottom: 4vh; margin-top: 4vh;"/>
              <img :src="tree2" class="h-60vh w-auto mx-auto" style="object-fit: cover; margin-bottom: 4vh; margin-top: 4vh;"/>
            </div>
          </div>
  </div>
  <div class="col-span-12 w-full" style="background-color: white; height: auto; color: white;">
  <div class="flex-col justify-around h-max">
            <div class="wrap-content-screen-size w-max justify-around flex-wrap">
              <img :src="landscape" class="h-40vh w-80vw mx-auto" style="object-fit: cover; margin-bottom: 4vh; margin-top: 4vh;"/>
            </div>
          </div>
  </div>
    <div class="col-span-12 w-full" style="background-color: white; height: auto; color: white;">
  <div class="flex-col justify-around h-max">
            <div class="wrap-content-screen-size w-max justify-between flex-wrap">
              <img :src="dog" class="h-40vh w-auto mx-auto" style="object-fit: cover; margin-bottom: 4vh; margin-top: 4vh;"/>
              <img :src="dogg" class="h-40vh w-auto mx-auto" style="object-fit: cover; margin-bottom: 4vh; margin-top: 4vh;"/>
            </div>
          </div>
  </div>
  <div class="col-span-12 w-full" style="background-color: yellow; height: 6rem; color: white;">
  footer :)
  </div>
  </div>
</div>
</template>
<script>
import art from '../assets/art.png';
import bird from '../assets/bird.jpg';
import cloud from '../assets/cloud.jpg';
import dog from '../assets/dog.jpg';
import dogg from '../assets/dogg.jpg';
import landscape from '../assets/landscape.jpg';
import smile from '../assets/smile.jpg';
import spider from '../assets/spider.jpg';
import tree from '../assets/tree.jpg';
import tree1 from '../assets/tree1.jpg';
import tree2 from '../assets/tree2.jpg';


export default {
  name: 'HomeRouter',
  props: {
    msg: String
  },
 data() {
  return {
    none: false,
    art,
    bird,
    cloud,
    dog,
    dogg,
    landscape,
    smile,
    spider,
    tree,
    tree1,
    tree2,
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

  .wrap-content-screen-size {
  display: flex;
  flex-direction: column;
  }

@media screen and (min-width: 510px) {
  .wrap-content-screen-size {
  display: flex;
  flex-direction: row;
  }
}
</style>
