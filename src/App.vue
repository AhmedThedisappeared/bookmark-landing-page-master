<template>
  <div class="wrapper">
    <Navbar />
    <Hero />
    <Features />
    <Extensions/>
    <Frequently/>
    <SingUp/>
    <Footer/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Features from './components/Features.vue'
import Extensions from './components/Extensions.vue'
import Frequently from './components/Freguently.vue'
import SingUp from './components/SingUp.vue';
import Footer from './components/Footer.vue';
export default {
  data() {
    return {

    }
  },
  components: {
    Navbar,
    Hero,
    Features,
    Extensions,
    Frequently,
    SingUp,
    Footer
  }
}
</script>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Rubik:wght@400;500&display=swap');
:root {
  --Soft-Blue: hsl(231, 69%, 60%);
  --Soft-Red: hsl(0, 94%, 66%);
  --Grayish-Blue: hsl(229, 8%, 60%);
  --Very-Dark-Blue: hsl(229, 31%, 21%);
}
* {
  box-sizing: border-box;
  padding: 0;
  margin: 0;
  font-family: 'Rubik', sans-serif;
}
a {
  text-decoration: none;
  color:#333;
}
ul {
  list-style: none;
}
img {
  max-width: 100%;
}
#app {
  width: 100%;
  min-height: 100vh;
  overflow: hidden;
  .wrapper {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
  }
}
/* Utility classes */
.container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 1.5rem;
}
.container-sm {
    max-width: 550px;
    margin: 0 auto;
    padding: 0 1.5rem;
}
.flex {
  display: flex;
}
.flex-column {
  flex-direction: column;
}
/* Buttons */
.btn {
  padding: 1rem 2rem;
  font-weight: 500;
  text-decoration: none;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  text-align: center;
  transition: 0.5s ease-in-out;
  vertical-align: middle;
  // box-shadow: 0 5px 10px 0 #ccc;
  white-space: nowrap;
  font-size: 14px;
  @media (max-width:768px) {
    padding:  16px 20px;
  }
}
.btn-light {
  color: #333;
  outline: 2px solid #f0f0f0;
  &:hover {
    background-color: #fff;
    color: #333;
    outline: 2px solid #333;
  }
}
.btn-primary {
  background: var(--Soft-Blue);
  color: #fff;
  &:hover {
    background-color: #fff;
    color: var(--Soft-Blue);
    outline: 2px solid var(--Soft-Blue);
  }
}
.btn-danger {
  background: var(--Soft-Red);
  text-transform: uppercase;
  color: #fff;
  font-weight: 500;
  letter-spacing: 1px;
  &:hover {
    background-color: #fff;
    color: var(--Soft-Red);
    outline: 2px solid var(--Soft-Red);
  }
}
.btn-block {
  display: block;
  width: 100%;
}

</style>
