<template>
  <div class="greeting-container">
    <h1 class="text-3xl font-bold mb-2">{{ greeting }}</h1>
    <p class="text-xl">{{ timeMessage }}</p>
  </div>
</template>

<script>
export default {
  name: "GreetingMessage",
  data() {
    return {
      currentHour: new Date().getHours()
    };
  },
  computed: {
    greeting() {
      if (this.currentHour < 12) {
        return "Good Morning!";
      } else if (this.currentHour < 18) {
        return "Good Afternoon!";
      } else {
        return "Good Evening!";
      }
    },
    timeMessage() {
      return `It's currently ${new Date().toLocaleTimeString()}`;
    }
  }
};
</script>