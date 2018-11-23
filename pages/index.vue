<template>
  <section class="container">
    <div>
      <logo/>
      <h2 class="subtitle">
        My First Project
      </h2>
      <div class="links">
        <nuxt-link id="text" to="/users">View Users</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script>

</script>

<style>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
#text{
  text-decoration: none;
  background-color: #2980b9;
  padding: 20px; 
  color: white;
}
#text:hover{
  box-shadow: 2px 2px 6px gray;
}
</style>
