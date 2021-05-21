<template>
  <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
      <!-- Container wrapper -->
      <div class="container">
        <!-- Navbar brand -->
        <router-link class="navbar-brand" to="/">Rock Store<i class="fas fa-meteor"></i> </router-link>

        <!-- Toggle button -->
        <button
          class="navbar-toggler"
          type="button"
          data-mdb-toggle="collapse"
          data-mdb-target="#navbarSupportedContent"
          aria-controls="navbarSupportedContent"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <i class="fas fa-bars"></i>
        </button>

        <!-- Collapsible wrapper -->
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <!-- Left links -->
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">        
          </ul>
          <!-- Left links -->

          <!-- Search form -->
          <ul class="navbar-nav">

            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown"
                href="#"
                id="navbarDropdown"
                role="button"
                data-mdb-toggle="dropdown"
                aria-expanded="false"
              >
                <i class="fas fa-shopping-cart"></i>
                <span v-show="cartItemCount" class="badge rounded-pill badge-notification bg-danger">{{ cartItemCount }}</span>
              </a>
              <!-- Dropdown menu -->
              <ul class="dropdown-menu dropdown-menu-end shopping-cart" aria-labelledby="navbarDropdown">
                <ShoppingCart />
              </ul>
            </li>

          </ul>
        </div>
        <!-- Collapsible wrapper -->
      </div>
      <!-- Container wrapper -->
    </nav>
    <!-- Navbar -->
</template>

<script>
import { mapGetters } from 'vuex'
import ShoppingCart from './shoppingCart/ShoppingCart'
export default {
  components: {
    ShoppingCart
  },
  computed: {
    ...mapGetters(['loggedIn']),
    ...mapGetters(['cartItemCount'])
  }

}
</script>

<style scoped>
  .shopping-cart {
    min-width: 450px;
  }
</style>