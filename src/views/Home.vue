<template>
   <div class="content">
      <h1 class="page-title">My Vehicles</h1>
      <div class="car-container" v-if="vehicles.length > 0">
         <div class="card" style="width: 18rem;" v-for="vehicle in vehicles" :key="vehicle.id">
            <img src="car1.jpg" class="card-img-top" />
            <div class="card-body">
               <h5 class="card-title">{{ vehicle.model }}</h5>
               <h6 class="card-subtitle mb-2 text-muted">{{ vehicle.year }}</h6>
            </div>
            <ul class="list-group list-group-flush">
               <li class="list-group-item"> <strong>Miles:</strong> {{ vehicle.miles }}</li>
               <li class="list-group-item"> <strong>License Plate:</strong> {{ vehicle.licensePlate }}</li>
               <li class="list-group-item"> <strong>Gas Mileage:</strong> {{ vehicle.gasMileage }} MPG</li>
            </ul>
         </div>
      </div>
      <div class="car-container" v-else>No Vehicles Have Been Added</div>
      <div class="add-vehicle">
         <router-link class="btn btn-primary" to="add-vehicle">
            Add New Vehicle
         </router-link>
      </div>
   </div>
</template>

<script>
export default {
   name: "Home",
   computed: {
      vehicles() {
         return this.$root.$data.vehicles;
      },
   },
};
</script>

<style scoped>
.car-container {
   display: flex;
   flex-wrap: wrap;
   gap: 20px;
   padding: 30px;
   justify-content: center;
}

.car-container .card {
   min-width: 200px;
}

.add-vehicle {
   display: flex;
   justify-content: center;
   margin-bottom: 30px;
}
</style>
