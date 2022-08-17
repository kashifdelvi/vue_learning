<template>
  <div class="container">
    <table class="table bg-success">
      <tr>
        <td>Name</td>
        <td>{{address.name}}</td>
      </tr>
      <tr>
        <td>Country</td>
        <td>{{address.country}}</td>
      </tr>
      <tr>
        <td>City</td>
        <td>{{address.city}}</td>
      </tr>
      <tr>
        <td>pin</td>
        <td>{{address.pin}}</td>
      </tr>
    </table>

    <div class="bg-primary text-white text-center p-2">
      {{address.name}},{{address.country}},{{address.city}},{{address.pin}}
    </div>


    <input 
      name="name"
      type="text"
      @change="handleChange"
      :value="address.name"
    />
    <input 
      name="country"
      type="text"
      @change="handleChange"
      :value="address.country"
    />
    <input 
      name="city"
      type="text"
      @change="handleChange"
      :value="address.city"
    />
    <input 
      name="pin"
      type="text"
      @change="handleChange"
      :value="address.pin"
    />

  </div>
</template>

<script>
    import "bootstrap/dist/css/bootstrap.min.css";
    export default {
      name: 'KashifContainer',
      data(){
        return {
          address:{
            'name':'kashif',
            'country':'India',
            'city':'Bangalore',
            'pin':560032
          }
        }
      },
      methods:{
        handleChange(event){
          const field = event.target.name;
          this.$data.address[field] = event.target.value;
        }
      }
    }
</script>
