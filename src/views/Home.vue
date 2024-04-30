<script>
import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap/dist/js/bootstrap.bundle.min.js'
import { RouterLink } from 'vue-router'

export default {
  name: 'App',
  components: {},
  methods: {
    toggleHeader
  }
}

function toggleHeader() {
  var header = document.querySelector('header')
  header.classList.toggle('d-none')
}
</script>
<template>
  <div>
    <div class="collapse" id="navbarHeader">
      <div class="container">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          fill="currentColor"
          color="white"
          data-bs-toggle="collapse"
          data-bs-target="#navbarHeader"
          class="bi bi-x-lg"
          viewBox="0 0 16 16"
          @click="toggleHeader"
        >
          <path
            d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8z"
          />
        </svg>
        <div class="row">
          <div class="col-sm py-4">
            <ul class="hidden-list list-unstyled d-flex flex-column align-items-center">
              <li><a href="#" class="text-white text-decoration-none">HOME</a></li>
              <li><a href="#" class="text-white text-decoration-none">ABOUT US</a></li>
              <li><a href="#" class="text-white text-decoration-none">SDU ALUMNI</a></li>
              <li><a href="#" class="text-white text-decoration-none">CLUBS</a></li>
              <li><a href="#" class="text-white text-decoration-none">CONTACTS</a></li>
              <li><a href="#" class="text-white text-decoration-none">QUOTE</a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
    <header style="padding: 0 3rem" class="py-3 mb-4 border-bottom">
      <div
        class="d-flex flex-wrap align-items-center justify-content-center justify-content-md-between"
      >
        <div class="navbar hidden-navbar navbar-dark">
          <div class="container">
            <button
              class="navbar-toggler"
              type="button"
              data-bs-toggle="collapse"
              data-bs-target="#navbarHeader"
              aria-controls="navbarHeader"
              aria-expanded="false"
              aria-label="Toggle navigation"
              @click="toggleHeader"
            >
              <span class="navbar-toggler-icon"></span>
            </button>
          </div>
        </div>

        <div class="col-md-3 mb-2 mb-md-0">
          <a href="/" class="d-inline-flex link-body-emphasis text-decoration-none">
            <svg class="bi" width="70" height="70" role="img" aria-label="Bootstrap">
              <image xlink:href="../assets/sdu_logo.png" width="70" height="70" />
            </svg>
          </a>
        </div>

        <ul
          class="nav items-visibility col-12 col-lg-auto me-lg-auto mb-2 justify-content-center mb-md-0"
        >
          <RouterLink class="nav-link px-2 link-secondary" to="/home">HOME</RouterLink>
          <RouterLink class="nav-link text-white" to="/about">ABOUT US</RouterLink>
          <RouterLink class="nav-link text-white" to="#">SDU ALUMNI</RouterLink>
          <RouterLink class="nav-link text-white" to="#">CLUBS</RouterLink>
          <RouterLink class="nav-link text-white" to="#">CONTACTS</RouterLink>
          <RouterLink class="nav-link text-white" to="#">QUOTE</RouterLink>
        </ul>

        <form class="col-12 col-lg-auto mb-3 mb-lg-0 me-lg-3 search-form" role="search">
          <!-- Icon -->
          <button type="button" class="btn btn-search-icon">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-search"
              viewBox="0 0 16 16"
            >
              <path
                d="M10.832 9.43a5.5 5.5 0 1 0-1.402 1.402l3.585 3.585a1 1 0 0 0 1.414-1.414l-3.587-3.587z"
              />
              <path
                d="M2 6.5a4.5 4.5 0 0 1 4.5-4.5 1 1 0 0 1 0 2A2.5 2.5 0 0 0 3.5 6.5a1 1 0 0 1-2 0z"
              />
            </svg>
          </button>

          <!-- Input -->
          <input
            type="search"
            class="form-control search-input"
            placeholder="Search..."
            aria-label="Search"
          />
        </form>

        <div class="text-end">
          <button type="button" class="btn text-white" data-bs-toggle="button">SIGN IN</button>
        </div>
      </div>
    </header>
  </div>
  <body class="d-flex flex-column h-100 text-bg-dark">
    <div class="cover-container d-flex w-100 h-100 text-white mx-auto flex-column">
      <main class="px-3 d-flex flex-column justify-content-center">
        <h1>SDU DIARY</h1>
        <p class="lead">The best knowledge is only here</p>
        <p class="lead">
          <a href="#" class="btn btn-lg fw-bold border-white text-white btn-learn-more"
            >Learn more
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="16"
              height="16"
              fill="currentColor"
              class="bi bi-arrow-right"
              viewBox="0 0 16 16"
            >
              <path
                fill-rule="evenodd"
                d="M1 8a.5.5 0 0 1 .5-.5h11.793l-3.147-3.146a.5.5 0 0 1 .708-.708l4 4a.5.5 0 0 1 0 .708l-4 4a.5.5 0 0 1-.708-.708L13.293 8.5H1.5A.5.5 0 0 1 1 8"
              />
            </svg>
          </a>
        </p>
      </main>
    </div>
    <!-- </div> -->
  </body>
</template>

<style>
body {
  text-shadow: 0 0.05rem 0.1rem rgba(0, 0, 0, 0.5);
  box-shadow: inset 0 0 5rem rgba(0, 0, 0, 0.5);
  background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),
    url('../assets/sdu_background.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

html {
  height: 100%;
}

.collapse {
  background-color: #140040;
  padding: 1rem;
}

.hidden-list {
  gap: 2rem;
}

.cover-container {
  display: flex;
  flex-direction: column;
  gap: 10rem;
  padding: 1rem 3rem;
}

.hidden-navbar {
  display: none;
}

@media screen and (max-width: 1200px) {
  .hidden-navbar {
    display: block;
  }

  .items-visibility {
    display: none;
  }
}

.bd-placeholder-img {
  font-size: 1.125rem;
  text-anchor: middle;
  -webkit-user-select: none;
  -moz-user-select: none;
  user-select: none;
}

@media (min-width: 768px) {
  .bd-placeholder-img-lg {
    font-size: 3.5rem;
  }
}

.b-example-divider {
  width: 100%;
  height: 3rem;
  background-color: rgba(0, 0, 0, 0.1);
  border: solid rgba(0, 0, 0, 0.15);
  border-width: 1px 0;
  box-shadow:
    inset 0 0.5em 1.5em rgba(0, 0, 0, 0.1),
    inset 0 0.125em 0.5em rgba(0, 0, 0, 0.15);
}

.b-example-vr {
  flex-shrink: 0;
  width: 1.5rem;
  height: 100vh;
}

.bi {
  vertical-align: -0.125em;
  fill: currentColor;
}

.nav-scroller {
  position: relative;
  z-index: 2;
  height: 2.75rem;
  overflow-y: hidden;
}

.nav-scroller .nav {
  display: flex;
  flex-wrap: nowrap;
  padding-bottom: 1rem;
  margin-top: -1px;
  overflow-x: auto;
  text-align: center;
  white-space: nowrap;
  -webkit-overflow-scrolling: touch;
}

.search-form {
  display: flex;
}

.search-input {
  width: 0;
  opacity: 0;
  transition:
    width 0.3s,
    opacity 0.3s;
}

.btn-search-icon {
  padding: 0;
  background-color: transparent;
  border: none;
}

.btn-search-icon svg {
  fill: white;
  transition: fill 0.3s;
}

.search-form:hover .search-input {
  width: auto;
  opacity: 1;
}

.search-form:hover .btn-search-icon svg {
  fill: #6c757d; /* Change color when hovered */
}

.btn-bd-primary {
  --bd-violet-bg: #712cf9;
  --bd-violet-rgb: 112.520718, 44.062154, 249.437846;

  --bs-btn-font-weight: 600;
  --bs-btn-color: var(--bs-white);
  --bs-btn-bg: var(--bd-violet-bg);
  --bs-btn-border-color: var(--bd-violet-bg);
  --bs-btn-hover-color: var(--bs-white);
  --bs-btn-hover-bg: #6528e0;
  --bs-btn-hover-border-color: #6528e0;
  --bs-btn-focus-shadow-rgb: var(--bd-violet-rgb);
  --bs-btn-active-color: var(--bs-btn-hover-color);
  --bs-btn-active-bg: #5a23c8;
  --bs-btn-active-border-color: #5a23c8;
}

.bd-mode-toggle {
  z-index: 1500;
}

.bd-mode-toggle .dropdown-menu .active .bi {
  display: block !important;
}

/*
    * Globals
    */

/* Custom default button */
.btn-light,
.btn-light:hover,
.btn-light:focus {
  color: #333;
  text-shadow: none; /* Prevent inheritance from `body` */
}

/*
    * Base structure
    */

/*
    * Header
    */

.nav-masthead .nav-link {
  color: rgba(255, 255, 255, 0.5);
  border-bottom: 0.25rem solid transparent;
}

.nav-masthead .nav-link:hover,
.nav-masthead .nav-link:focus {
  border-bottom-color: rgba(255, 255, 255, 0.25);
}

.nav-masthead .nav-link + .nav-link {
  margin-left: 1rem;
}

.nav-masthead .active {
  color: #fff;
  border-bottom-color: #fff;
}

.btn-learn-more {
  border-color: white; /* Set the border color to white */
  color: white; /* Set the text color to white */
  background-color: transparent; /* Set the background color to transparent */
  transition: background-color 0.5s;
  border-radius: 1rem;
}

.btn-learn-more:hover {
  background-color: #140040; /* Change background color to violet on hover */
}
</style>
