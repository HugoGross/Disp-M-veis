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
      flex-direction:column;
      position: center;
      background-color: rgba(0, 2, 121, 0.884);
      box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
      border-radius: 10px;
      right: 0;
      text-align: right;
      padding: 10px 16px;
      align-items: center;
      
}
footer p{
  position: center;
  display:flex;
  color: rgb(255, 255, 255);
}
</style>