<template>
  <div>

    <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-dark">
<!--      <a 
        class="navbar-brand" 
        href="#">Vue course app</a> -->
      <button 
        class="navbar-toggler" 
        type="button" 
        data-toggle="collapse" 
        data-target="#navbarCollapse" 
        aria-controls="navbarCollapse" 
        aria-expanded="false" 
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"/>
      </button>
      <div 
        class="collapse navbar-collapse" 
        id="navbarCollapse">
        <ul class="navbar-nav mr-auto">
          <router-link 
            tag="li" 
            to="/" 
            exact 
            active-class="active">
            <a 
              class="nav-link" 
              href="#">Main</a>
          </router-link>
          <router-link 
            tag="li" 
            to="/users" 
            exact 
            active-class="active">
            <a 
              class="nav-link" 
              href="#">Users list</a>
          </router-link>
          <router-link 
            tag="li" 
            to="/add" 
            exact 
            active-class="active">
            <a 
              class="nav-link" 
              href="#">Add user</a>
          </router-link>
        </ul>
      </div>
    </nav>

    <main
      id="app"
      role="main" 
      class="container"       
    >
       <router-view/>
    </main>

  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
export default {
  name: 'App'
}
</script>

<style scoped>
#app {
  margin-top: 60px;
}
</style>