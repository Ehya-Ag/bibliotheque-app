<template>
    <div>
      <nav class="navbar navbar-expand-lg navbar-dark bg-info fixed-top">
        <div class="container">
          <!-- Brand -->
          <router-link to="/" class="navbar-brand">
            <strong>Bibliothèque</strong>
          </router-link>
    
          <!-- Toggler button -->
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarTogglerDemo02"
            aria-controls="navbarTogglerDemo02"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <i class="fas fa-bars"></i>
          </button>
    
          <!-- Navbar links -->
          <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <router-link
                  to="/livres"
                  class="nav-link"
                  active-class="active"
                  aria-current="page"
                >
                  <i class="fas fa-book me-2"></i> Livres
                </router-link>
              </li>
              <li class="nav-item">
                <router-link
                  to="/membres"
                  class="nav-link"
                  active-class="active"
                >
                  <i class="fas fa-user me-2"></i> Membres
                </router-link>
              </li>
              <li class="nav-item">
                <router-link
                  to="/prets"
                  class="nav-link"
                  active-class="active"
                >
                  <i class="fas fa-hand-holding"></i> Prêts
                </router-link>
              </li>
            </ul>
    
            <!-- Search form -->
            <form class="d-flex input-group w-auto me-3">
              <input
                type="search"
                class="form-control"
                placeholder="Rechercher"
                aria-label="Search"
              />
              <button
                class="btn btn-outline-light"
                type="button"
              >
                <i class="fas fa-search"></i>
              </button>
            </form>
    
            <!-- Profile dropdown -->
            <ul class="navbar-nav d-flex flex-row">
              <li class="nav-item dropdown">
                <a
                  class="nav-link dropdown-toggle text-white"
                  href="#"
                  id="navbarDropdown"
                  role="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  <i class="fas fa-user"></i>
                </a>
                <ul class="dropdown-menu dropdown-menu-end" aria-labelledby="navbarDropdown">
                  <li><router-link to="/profile" class="dropdown-item">Mon compte</router-link></li>
                  <li><a class="dropdown-item" href="#">Déconnexion</a></li>
                </ul>
              </li>
            </ul>
          </div>
        </div>
      </nav>
      <!-- Spacer to prevent content from hiding behind the fixed navbar -->
      <div class="navbar-spacer"></div>
    </div>
  </template>
  
  <script setup>

  </script>
  
  <style scoped>
  /* .navbar {
    background-color: #17a2b8; 
    padding: 1rem 1rem; 
    z-index: 1000; 
  } */
  

  .navbar-brand {
    font-size: 2rem;
    font-weight: bold;
    color: gold;
  }
  
  .nav-link {
    font-size: 1.5rem;
  }
  
  .nav-link i {
    font-size: 1.5rem; 
  }
  
  .btn-outline-light {
    color: #ffffff;
    border-color: #ffffff;
  }
  
  .btn-outline-light:hover {
    background-color: #ffffff;
    color: #17a2b8;
  }
  

  .navbar-spacer {
    height: 50px;
  }
  
  .dropdown-menu {
    border-radius: 0.5rem;
  }
  
  </style>
  