<template>
  <div>
    <div style="height: 65px" />
    <b-navbar toggleable="md" fixed="top" type="dark" variant="dark">
      <b-container class="px-0">
        <b-navbar-brand to="/">
          <img
            src="/icon.png"
            height="45px"
            width="50px"
            alt="Hutchinson logo"
            class="bg-light p-1 rounded"
          />
          <!-- <span class="ml-2">
            <fa :icon="['fas', 'home']" />
          </span> -->
          <strong> S-BETS.COM |</strong>
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse">
          <template>
            <div class="text-light">
              <fa :icon="['fas', 'bars']" style="font-size: 30px" />
            </div>
          </template>
        </b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item-dropdown text="Current Bets">
              <b-dropdown-item to="/current-bets/ligue1">French Ligue 1</b-dropdown-item>
              <b-dropdown-item to="/currents-bets/liga">Spain Liga</b-dropdown-item>
            </b-nav-item-dropdown>
            <b-nav-item-dropdown text="Past Bets">
              <b-dropdown-item to="/past-bets/ligue1">French Ligue 1</b-dropdown-item>
              <b-dropdown-item to="/past-bets/liga">Spain Liga</b-dropdown-item>
            </b-nav-item-dropdown>
            <template v-if="isLoggedIn">
              <b-nav-item to="/my-bets">
                <fa :icon="['fas', 'file-invoice-dollar']" />
                My Bets
              </b-nav-item>
              <b-nav-item to="/profile">
                <fa :icon="['fas', 'user']" />
                Profile
              </b-nav-item>
              <b-nav-item @click="signout()">
                <fa :icon="['fas', 'sign-out-alt']" />
                Sign Out
              </b-nav-item>
            </template>
            <template v-else>
              <b-nav-item to="/signin">
                <fa :icon="['fas', 'sign-in-alt']" />
                Sign In
              </b-nav-item>
            </template>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
  </div>
</template>

<script>
export default {
  computed: {
    isLoggedIn() {
      return true
    },
  },
  methods: {
    signout() {
      alert('Signout')
    },
  },
}
</script>
