<template>
  <v-container>
    <!-- <v-layout> -->
    <h1>Weather App</h1>
    <!-- <v-flex>
      <v-card>
        <v-card-text>Here is the card</v-card-text>
      </v-card>
    </v-flex>
    <v-col class="mt-4">
      <v-form @submit.prevent="getWeatherInfo">
        <v-text-field
          v-model="city"
          label="Enter City Name"
          solo
        ></v-text-field>
      </v-form>
    </v-col> -->
    <!-- </v-layout> -->
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      city: 'Lagos',
      weather: {}
    }
  },
  created() {
    this.getWeatherInfo()
  },

  methods: {
    getWeatherInfo() {
      this.$axios
        .$get(
          `https://api.openweathermap.org/data/2.5/weather?q=${this.city}&appid=ddb956415e4c89646c1fe66f214ec94a`
        )
        .then((res) => {
          this.weather = res
          /* eslint-disable-next-line */
          console.log(this.weather.id)
        })
        .catch(
          /* eslint-disable-next-line */
          (err) => console.log(err)
        )
    }
  }
}
</script>
