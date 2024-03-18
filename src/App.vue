<script setup>
  import { useMonitor } from '@/composables/monitor';
  
  const { menu } = useMonitor();
</script>

<template>
  <div>
    <component :is="menu" />
    <main>
      <router-view />
    </main>
    <footer>
      <ul :class="menuAberto ? 'menu' : ''">
        <li>Home</li>
        <li>Eletrônicos</li>
        <li>Jóias</li>
        <li>Masculino</li>
        <li>Feminino</li>
      </ul>
      <p>Copyright &copy; 2024</p>
    </footer>
  </div>
</template>

<style scoped>
footer {
  display: flex;
    justify-content:center;
    align-items: center;
    padding: 2rem;
    background-color: #EEEEEE;
    grid-area: footer;
}
footer ul{
  padding-right: 3rem;
    display: flex;
    gap: 4rem;
    align-items: center;
}
</style>