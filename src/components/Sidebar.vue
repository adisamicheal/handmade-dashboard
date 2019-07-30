<template>
    <aside class="app-sidebar">
    <div class="logo-part">
      <img src="../assets/crestschool.png"> <p class="name">Handmaid's International</p>
    </div>
    
      <ul class="categories-list">
        <li class="category" v-for="category in categories" :key="category">
          {{ category.charAt(0).toUpperCase() + category.slice(1) }}
        </li>
      </ul>
      <hr class="line">
    </aside>
</template>

<script>

export default {
  name: 'Sidebar',

  data() {
    return {
      categories: [
        "dashboard",
        "students",
        "employees",
        "guardian",
        "attendance",
        "finance",
        "subject",
        "batches",
        "report card",
        "sms",
        "events",
      ]
    }
  }
}
</script>

<style>

.logo-part{
  background-color: #ffffff;
  height: 70px;
}
.name{
  color: #000000;
  margin-top: -30px;
  padding-left: 40px;
}

.categories-list {
  padding: 3em 2em;
  list-style: none;
  margin: 0;
}

.category {
  padding: 0.5em 1em;
  margin-bottom: 0.5em;
}

.app-sidebar {
  background: linear-gradient(136.25deg, #1B75BB 0%, #00ADEE 100%);
  height: 100%;
  color: #ffffff;
  width: 265px;
}

.line{
  color: #ffffff;
}
</style>