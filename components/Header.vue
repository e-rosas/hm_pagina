<template>
  <div>
    <base-nav type="" transparent effect="" expand>
      <nuxt-link slot="brand" class="navbar-brand mr-lg-5" to="/">
        <img src="img/brand/Hm-logo-02.png" alt="logo" />
      </nuxt-link>

      <div slot="content-header" slot-scope="{ closeMenu }" class="row">
        <div class="col-6 collapse-brand">
          <a href="#">
            <img src="img/brand/Hm-logo-02.png" />
          </a>
        </div>
        <div class="col-6 collapse-close">
          <close-button @click="closeMenu"></close-button>
        </div>
      </div>

      <ul class="navbar-nav navbar-nav-hover align-items-lg-center">
        <base-dropdown class="nav-item">
          <a
            slot="title"
            href="#services"
            class="nav-link"
            data-toggle="dropdown"
            role="button"
          >
            <i class="fa fa-hospital-o d-lg-none"></i>
            <span class="nav-link-inner--text">SERVICES</span>
          </a>
          <a class="dropdown-item" href="#services">Dental</a>
          <a class="dropdown-item" href="#services">Surgeries</a>
          <a class="dropdown-item" href="#services">Medical Specialists</a>
          <a class="dropdown-item" href="#services">Hospitalization</a>
          <a class="dropdown-item" href="#services">Laboratory</a>
          <a class="dropdown-item" href="#services">Treatments</a>
        </base-dropdown>
        <li class="nav-item">
          <a class="nav-link nav-link-icon" href="http://dentimexico.com/">
            DENTALCENTER
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link nav-link-icon" href="#insurances">
            INSURANCES
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link nav-link-icon" href="#pricing">
            PRICING
          </a>
        </li>
        <li class="nav-item">
          <a
            class="nav-link nav-link-icon"
            href="https://www.youtube.com/watch?v=rUZd4YgJ9nI"
          >
            DIRECTIONS
          </a>
        </li>
        <li class="nav-item">
          <a class="nav-link nav-link-icon" href="#contact">
            CONTACT
          </a>
        </li>
        <li class="nav-item">
          <nuxt-link class="nav-link nav-link-icon" to="registro"
            >REGISTER</nuxt-link
          >
        </li>
      </ul>
      <ul class="navbar-nav align-items-lg-center ml-lg-auto">
        <li class="nav-item">
          <a
            class="nav-link nav-link-icon"
            href="mailto:info@hospitalmexico.org"
            target="_blank"
            rel="noopener"
            data-toggle="tooltip"
            title="Email Us"
          >
            <i class="fa fa-envelope"></i>
            <span class="nav-link-inner--text d-lg-none"
              >info@hospitalmexico.org</span
            >
          </a>
        </li>
        <li class="nav-item">
          <a
            class="nav-link nav-link-icon"
            href="tel:18003158714"
            target="_blank"
            rel="noopener"
            data-toggle="tooltip"
            title="Call Us"
          >
            <i class="fa fa-phone"></i>
            <span class="nav-link-inner--text d-lg-none">1 800 315 87 14</span>
          </a>
        </li>
        <li class="nav-item">
          <nuxt-link slot="brand" class="navbar-brand mr-lg-5" to="es">
            <span class="nav-link">Español</span>
          </nuxt-link>
        </li>
      </ul>
    </base-nav>
  </div>
</template>
<script>
import BaseNav from '~/components/BaseNav'
import BaseDropdown from '~/components/BaseDropdown'
import CloseButton from '~/components/CloseButton'

export default {
  components: {
    BaseNav,
    CloseButton,
    BaseDropdown
  }
}
</script>
<style></style>
