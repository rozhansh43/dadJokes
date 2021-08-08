<template>
  <div>
    <b-navbar toggleable="lg" type="light" variant="light" class="text-white">
      <b-navbar-brand href="#">
        NavBar
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse" >
      </b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item >
            <nuxt-link to="/">
              Home
            </nuxt-link>
          </b-nav-item>

          <b-nav-item>
            <nuxt-link to="/jokes">
              Jokes
            </nuxt-link>
          </b-nav-item>

          <b-nav-item>
            <nuxt-link to="/about">
              About
            </nuxt-link>
          </b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>

