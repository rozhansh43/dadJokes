<template>
  <div>
    <div>
      <b-navbar toggleable="lg" type="dark" variant="dark" class="text-white">
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
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>