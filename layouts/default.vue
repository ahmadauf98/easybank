<template>
  <div>
    <div class="container-md">
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
            <b-nav-item href="#">Careers</b-nav-item>
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

    <footer
      class="p-0 custom-footer d-flex align-items-center justify-content-center"
    >
      <div class="p-3 py-5 px-md-5 mx-auto container-md">
        <div class="px-2 px-md-0 my-4">
          <div class="row">
            <div class="col-12 col-md-4 mb-4 mb-md-0 text-center text-md-left">
              <div class="mb-4 mb-md-5">
                <img src="~/static/logo-white.svg" alt="..." />
              </div>
              <div
                class="d-inline"
                v-for="social in socials"
                :key="social.name"
              >
                <a class="mx-2 mx-md-0 mr-md-3" href="#">
                  <img :src="social.logo" alt="..."
                /></a>
              </div>
            </div>
            <div class="col-12 col-md-2 text-center text-md-left">
              <div class="d-block mb-2" v-for="link in Llinks">
                <a class="link-style" :href="link.href">{{ link.name }}</a>
              </div>
            </div>
            <div class="col-12 col-md-2 text-center text-md-left">
              <div class="d-block mb-2" v-for="link in Rlinks">
                <a class="link-style" :href="link.href">{{ link.name }}</a>
              </div>
            </div>
            <div class="col-12 col-md-4 mt-4 mt-md-0 text-center">
              <div class="mb-4">
                <b-button class="custom-btn px-4" size="lg">
                  Request Invite
                </b-button>
              </div>
              <div class="px-4">
                <p class="text-white">
                  &copy; Challenge by
                  <a
                    class="link-style"
                    href="https://www.frontendmentor.io?ref=challenge"
                    target="_blank"
                    rel="noopener"
                    >Frontend Mentor</a
                  >. Coded by
                  <a
                    class="link-style "
                    href="https://twitter.com/aufnasa_"
                    target="_blank"
                    rel="noopener"
                    >@aufnasa_</a
                  >
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      socials: [
        { name: 'facebook', logo: 'icon-facebook.svg' },
        {
          name: 'youtube',
          logo: 'icon-youtube.svg',
        },
        {
          name: 'twitter',
          logo: 'icon-twitter.svg',
        },
        {
          name: 'pinterest',
          logo: 'icon-pinterest.svg',
        },
        {
          name: 'instagram',
          logo: 'icon-instagram.svg',
        },
      ],
      Llinks: [
        {
          name: 'About us',
          href: '#',
        },
        {
          name: 'Contact',
          href: '#',
        },
        {
          name: 'Blog',
          href: '#',
        },
      ],
      Rlinks: [
        {
          name: 'Careers',
          href: '#',
        },
        {
          name: 'Support',
          href: '#',
        },
        {
          name: 'Privacy Policy',
          href: '#',
        },
      ],
    }
  },
}
</script>

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

.custom-btn:hover {
  background-image: linear-gradient(
    to right,
    rgb(49, 211, 92, 0.5),
    rgb(43, 183, 218, 0.5)
  );
  border-radius: 50px;
  border: none;
  font-size: 16px;
  font-weight: 500;
}

.custom-footer {
  background-color: #2d314d;
  padding: 1em 2em;
  min-height: 20vh;
}

.link-style {
  color: white;
  font-weight: 400;
  text-decoration: none;
}

.link-style:hover {
  color: white;
  font-weight: 500;
  text-decoration: none;
}

/* Medium devices (tablets, 992px and up) */
@media only screen and (min-width: 992px) {
  .custom-nav {
    background-color: #ffffff;
    padding: 1em 2em;
  }
}
</style>
