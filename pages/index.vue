<template>
  <div class="container-fluid p-0">
    <div
      id="content-1"
      class="p-3 py-5 p-md-5 mx-auto d-flex align-items-center justify-content-center"
    >
      <div class="row">
        <div
          class="col-12 col-md-6 d-flex d-md-none mb-4 p-0 justify-content-center"
        >
          <img class="img-mockups" src="~/static/image-mockups.png" alt="..." />
        </div>
        <div class="col-12 col-md-6 px-5">
          <div class="title mb-4">
            <p
              class="h1 font-weight-normal text-center text-md-left d-flex d-md-none"
            >
              Next generation digital banking
            </p>
            <p
              class="display-4 font-weight-normal text-center text-md-left d-none d-md-flex"
            >
              Next generation digital banking
            </p>
          </div>
          <div class="sub-title mb-4 pr-md-5 text-grey">
            <p class="lead text-center text-md-left">
              Take your financial life online. Your Easybank account will be a
              one-stop-shop for spending, saving, budgeting, investing, and much
              more.
            </p>
          </div>
          <div class="sub-btn text-center text-md-left">
            <b-button class="custom-btn px-4" size="lg"
              >Request Invite</b-button
            >
          </div>
        </div>
        <div class="col-12 col-md-6 d-none d-md-flex">
          <img class="img-mockups" src="~/static/image-mockups.png" alt="..." />
        </div>
      </div>
    </div>

    <div
      id="content-2"
      class="p-3 py-5 p-md-5 mx-auto d-block d-flex align-items-center justify-content-center"
    >
      <div class="px-md-5">
        <div class="row mb-5">
          <div class="col-12 col-md-6">
            <div class="title mb-4">
              <p class="h1 font-weight-normal text-center text-md-left">
                Why choose Easybank?
              </p>
            </div>
            <div class="sub-title text-grey">
              <p class="lead text-center text-md-left">
                We leverage Open Banking to turn your bank account into
                financial hub. Control your finances like never before.
              </p>
            </div>
          </div>
        </div>
        <div class="row">
          <div
            class="col-12 col-md-3 mb-5 mb-md-0"
            v-for="item in content"
            :key="item.title"
          >
            <div class="icon mb-4 text-center text-md-left">
              <img :src="item.icon" alt="..." />
            </div>
            <div class="title mb-4">
              <p class="h3 font-weight-normal text-center text-md-left">
                {{ item.title }}
              </p>
            </div>

            <div class="sub-title text-grey text-center text-md-left pr-md-4">
              <p class="h5 font-weight-light">
                {{ item.subtitle }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content: [
        {
          icon: 'icon-online.svg',
          title: 'Online Banking',
          subtitle:
            'Our modern web and mobile applications allow you to keep track of your finances wherever you are in the world.',
        },
        {
          icon: 'icon-budgeting.svg',
          title: 'Simple Budgeting',
          subtitle:
            "See exactly where your money goes each month. Receive notofocations when you're close to hitting your limits.",
        },
        {
          icon: 'icon-onboarding.svg',
          title: 'Fast Onboarding',
          subtitle:
            "We don't do brances. Open your account in minutes online and start taking control of you finances right away.",
        },
        {
          icon: 'icon-api.svg',
          title: 'Open API',
          subtitle:
            'Manage your savings, investments, pension, and much more from one account. Tracking your money has never been easier',
        },
      ],
    }
  },
}
</script>

<style scoped>
.text-grey {
  color: grey;
}

/* Small devices (mobile & Tablet, 992px and below) */
@media only screen and (max-width: 991px) {
  #content-1 {
    margin: 0;
    padding: 0;
    min-height: 100vh;
    background-color: #fafafa;
    background-image: url(~static/bg-intro-mobile.svg);
    background-size: 100%;
    background-repeat: no-repeat;
    background-position: center top;
  }

  #content-2 {
    min-height: 100vh;
    background-color: #f3f4f6;
  }

  .img-mockups {
    width: 90vw;
    height: 65vh;
  }
}

/* Large devices (desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  #content-1 {
    margin: 0;
    padding: 0;
    min-height: 60vh;
    background-color: #fafafa;
    background-image: url(~static/bg-intro-desktop.svg);
    background-size: 91%;
    background-repeat: no-repeat;
    background-position: 450% 50%;
  }

  #content-2 {
    margin: 0;
    padding: 0;
    min-height: 60vh;
    background-color: #f3f4f6;
  }

  .img-mockups {
    position: absolute;
    left: 5%;
    bottom: -70%;
  }
}

/* Extra large devices (large desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  #content-1 {
    margin: 0;
    padding: 0;
    min-height: 90vh;
    background-color: #fafafa;
    background-image: url(~static/bg-intro-desktop.svg);
    background-size: 91%;
    background-repeat: no-repeat;
    background-position: 450% 50%;
  }

  #content-2 {
    margin: 0;
    padding: 0;
    min-height: 70vh;
    background-color: #f3f4f6;
  }

  .img-mockups {
    position: absolute;
    left: 5%;
    bottom: -110%;
  }
}

/* 2K devices (2K desktops, 1920px and up) */
@media only screen and (min-width: 1920px) {
  #content-1 {
    margin: 0;
    padding: 0;
    min-height: 95vh;
    background-color: #fafafa;
    background-image: url(~static/bg-intro-desktop.svg);
    background-size: 91%;
    background-repeat: no-repeat;
    background-position: 450% 50%;
  }

  #content-2 {
    margin: 0;
    padding: 0;
    min-height: 75vh;
    background-color: #f3f4f6;
  }

  .img-mockups {
    position: absolute;
    left: 5%;
    bottom: -105%;
  }
}
</style>
