<template>
   <div class="content">
      <h1 class="page-title">Add Vehicle</h1>
      <form class="add-vehicle-form" v-on:submit.prevent="addVehicle">
         <div class="form-group">
            <label for="make">Vehicle Make/Model</label>
            <input class="form-control" id="make" aria-describedby="makeHelp" v-model="model" />
            <small id="makeHelp" class="form-text text-muted">Ex: Hyundai Accent</small>
         </div>
         <div class="form-group">
            <label for="year">Year</label>
            <input type="text" class="form-control" id="year" v-model="year" />
         </div>
         <div class="form-group">
            <label for="miles">Miles</label>
            <input type="text" class="form-control" id="miles" v-model="miles" />
         </div>
         <div class="form-group">
            <label for="license_plate">License Plate</label>
            <input type="text" class="form-control" id="license_plate" v-model="licensePlate" />
         </div>
         <div class="form-group">
            <label for="gas">Gas Mileage</label>
            <input type="text" class="form-control" id="gas" v-model="gasMileage" />
         </div>
         <button class="btn btn-primary">Submit</button>
      </form>
   </div>
</template>

<script>
export default {
   data() {
      return {
         model: "",
         year: "",
         miles: "",
         licensePlate: "",
         gasMileage: "",
      };
   },
   methods: {
      addVehicle() {
         this.$root.$data.vehicles.push({
            id: Math.floor(Math.random() * Math.floor(1000000)),
            model: this.model,
            year: this.year,
            miles: this.miles,
            licensePlate: this.licensePlate,
            gasMileage: this.gasMileage,
         });
         this.$router.push("/");
      },
   },
};
</script>

<style scoped>
.add-vehicle-form {
   margin-bottom: 20px;
}
</style>
