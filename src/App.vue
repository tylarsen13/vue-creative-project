<template>
   <div id="app">
      <nav class="navbar sticky-top navbar-expand-lg navbar-light bg-light">
         <router-link class="navbar-brand" to="/">Vehicle Maintenance Tracker</router-link>
         <button
            class="navbar-toggler"
            type="button"
            data-toggle="collapse"
            data-target="#navbarNavAltMarkup"
            aria-controls="navbarNavAltMarkup"
            aria-expanded="false"
            aria-label="Toggle navigation"
         >
            <span class="navbar-toggler-icon"></span>
         </button>
         <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
            <div class="navbar-nav mr-auto">
               <router-link class="nav-link active" to="/"
                  >Home
                  <span class="sr-only">(current)</span>
               </router-link>
               <router-link class="nav-link" to="/add-vehicle">Add Vehicle</router-link>
            </div>
            <router-link class="btn btn-light my-2 my-sm-0 pull-right" to="/login">Log In</router-link>
         </div>
      </nav>
      <div class="page">
         <router-view />
      </div>

      <div class="footer">
         <div>&copy;2020 Vehicle Maintenance Tracker</div>
         <div>
            <a href="https://github.com/tylarsen13/vue-creative-project">GitHub Repo</a>
         </div>
      </div>
   </div>
</template>

<style>
.bg-light {
   background-color: #ff564a !important;
}

.page {
   display: flex;
   flex-direction: column;
   justify-content: space-between;
   min-height: calc(100vh - 118px);
}

.footer {
   display: flex;
   background-color: #17191b;
   flex-direction: column;
   align-items: center;
   color: rgba(255, 255, 255, 0.5);
   padding: 10px;
   font-size: 14px;
}

.content {
   display: flex;
   flex-direction: column;
   align-items: center;
}

.page-title {
   text-align: center;
   margin-top: 30px;
}
</style>
