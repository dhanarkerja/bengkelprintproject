<template>
<div class="container">
    <div class="row">
        <div class="col-12">
            <h1 class="title text-center">Bengkel Print Indonesia</h1>
        </div>
        <div class="col-12">
            <header class="header d-flex justify-content-center">
                <ul>
                <li>
                    <nuxt-link to="/">Test 1</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/index2">Test 2</nuxt-link>
                </li>
                <li>
                    <nuxt-link to="/index3">Test 3</nuxt-link>
                </li>
                </ul>
            </header>
        </div>
  </div>
</div>
</template>

<script>
export default {
  name: "AppHeader"
};
</script>

<style>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
  padding-bottom: 1rem;
  border-bottom: 1px dotted #ccc;
}

.header .title {
  font-size: 3rem;
  color: #526488;
}

.header ul {
  display: flex;
}

.header a {
  display: inline-block;
  background: #333;
  color: #fff;
  padding: 0.3rem 1rem;
  margin-right: 0.5rem;
}
</style>