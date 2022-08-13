<template>
  <div>
    <section v-for="(username, index) in usernames" :key="index">
      <h3 @click="highlight_username">{{ username }}</h3>
    </section>
  </div>
</template>

<script>
export default {
  methods: {
    highlight_username(details) {
     let username = details[`target`][`innerText`];
     this.$root.$emit(`user_clicked`, username);
    },
  },

  data() {
    return {
      usernames: [`Gabriel`, `Natalia`, `Alex`, `Colleen`],
    };
  },
};
</script>

<style scoped></style>
