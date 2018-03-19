<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <ul>
      <li
        v-for="(blog, index) in blogs"
        v-bind:blog="blog"
        v-bind:index="index"
        v-bind:key="index"
        v-on:click="openArticle"
        >
        <a :href="'blogs/' + blog.id">
          <h3>{{ blog. title }}</h3>
          <p>{{ blog.texts }}</p>
        </a>
      </li>

    </ul>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      msg: 'Hello Cutie!',
      blogs: [
        {
          id: '0',
          title: 'How to get your owner\'s attention?',
          texts: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla',
        },
        {
          id: '1',
          title: 'How to get treats?',
          texts: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla',
        },
      ],
    };
  },
  methods: {
    openArticle: () => {
      // console.log('clicked');
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  font-weight: 500;
}
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
  width: 50%;
  margin: auto;
}
li {
  display: inline-block;
  margin: 0 1em;
}
li p {
  text-align: left;
}
a {
  text-decoration: none;
  color:inherit;
}
</style>
