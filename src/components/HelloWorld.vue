<template>
  <div class="hello">
    <img
      class="my-picture"
      alt="My Picture"
      src="../../utils/photos/website_profile_pic.jpeg"
    />
    <h1 class="message">{{ msg }}</h1>
    <p>
      I'm Burakhan. A Junior
      <img
        class="logo-python"
        alt="Python Logo"
        src="../../utils/photos/Python-Transparent-Background.png"
      />
      Developer.<br />
    </p>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 20px 0 10px 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.my-picture {
  width: 15rem;
  border-radius: 100%;
  height: 15rem;
  object-fit: cover;
}
.logo-python {
  width: 32px;
  height: 29px;
  object-fit: cover;
}

.message {
  margin-top: 10px;
}
</style>
