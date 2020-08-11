<template>
  <div>
    <div>
      <b-navbar class="custom-nav" toggleable="lg" sticky type="light">
        <b-navbar-brand href="#"
          ><img src="~/static/logo.svg" alt="..."
        /></b-navbar-brand>

        <b-navbar-toggle target="nav-collapse" size="md"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="custom-nav-list py-3 py-md-0">
            <b-nav-item href="#">Home</b-nav-item>
            <b-nav-item href="#">About</b-nav-item>
            <b-nav-item href="#">Contact</b-nav-item>
            <b-nav-item href="#">Blog</b-nav-item>
            <b-nav-item href="#">Carrers</b-nav-item>
          </b-navbar-nav>

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-button class="custom-btn px-4" size="lg"
              >Request Invite</b-button
            >
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>

    <div>
      <Nuxt />
    </div>
  </div>
</template>

<style>
.custom-nav {
  background-color: #ffffff;
  padding: 1em 2em;
}

.custom-nav-list {
  font-weight: 500;
}

.custom-btn {
  background-image: linear-gradient(to right, #31d35c, #2bb7da);
  border-radius: 50px;
  border: none;
  font-size: 16px;
  font-weight: 500;
}

/* Medium devices (tablets, 992px and up) */
@media only screen and (min-width: 992px)  {
  .custom-nav {
    background-color: #ffffff;
    padding: 1em 6em;
  }
}
</style>
