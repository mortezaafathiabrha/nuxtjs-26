<template>
  <div class="container">
    <h1 class="title">{{ message }}</h1>
    <p class="subtitle">Welcome to Nuxt.js</p>
    <p class="meta">Node.js {{ nodeVersion }}</p>
  </div>
</template>

<script setup lang="ts">
const message = ref("Hello World!");
const nodeVersion = useState("node-version", () =>
  import.meta.server ? process.version : "",
);

onMounted(() => {
  console.log("App mounted successfully!");
});
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.title {
  font-size: 4rem;
  font-weight: 700;
  color: white;
  margin: 0;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
}

.subtitle,
.meta {
  font-size: 1.5rem;
  color: rgba(255, 255, 255, 0.9);
  margin-top: 1rem;
}

.meta {
  font-size: 1rem;
}
</style>
