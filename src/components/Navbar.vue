<template>
  <nav>
    <ul class="menu">
      <div class="left">
        <li><router-link to="/">Home</router-link></li>
        <!-- <li><router-link to="/dashboard">Dashboard</router-link></li> -->
      </div>
      <div class="right">
        <li><router-link to="/signup">Sign Up</router-link></li>
        <li><router-link to="/signin">Sign In</router-link></li>
        <li><slot name="icon" class="icon"></slot></li>
      </div>
    </ul>
  </nav>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import '../assets/styles/styles.scss';
nav {
  position: relative;
  width: 100%;
  border-bottom: 1px solid rgba($color-1, 0.2);
  padding: 0 auto;
  font-size: 1.2rem;
  background-color: $white;
  .menu {
    list-style-type: none;
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
    padding: 1.2rem 1.5rem;
    margin: 0;
    border: none;
    li {
      display: inline-block;
      align-items: center;
      margin: 0 1rem;
      a {
        text-decoration: none;
        display: block;
        cursor: pointer;
        border-bottom: 2px solid transparent;
        display: inline;
        padding-bottom: 1rem;
        color: rgba($black, $alpha: 0.7);
      }
      a:hover {
        border-bottom-color: $color-1;
        transition: all 0.5s;
        color: $black;
      }
      .router-link-exact-active {
        border-bottom-color: $color-1;
        transition: all 0.5s;
        color: $black;
      }
    }
  }
}
</style>
