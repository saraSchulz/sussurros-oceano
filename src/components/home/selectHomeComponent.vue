<script setup>
</script>
<template>
  <section class="select">
    <ul>
      <li>
        <i class="mdi mdi-tsunami"></i>
        Exemplo
      </li>
      <img src="/public/Line-1.png" alt="line">
      <li>
        <i class="mdi mdi-fish"></i>
        Exemplo
      </li>
      <img src="/public/Line-1.png" alt="line">
      <li>
        <i class="mdi mdi-jellyfish"></i>
        Exemplo
      </li>
    </ul>
  </section>
</template>
<style scoped>
.select {
  width: 100%;
  padding: 80px 40px;

  & ul {
    display: flex;
    justify-content: space-around;
    gap: 2rem;
    padding: 1rem;

    & li {
      font-size: 2rem;
      text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.5);
      color: #000000;
    }
    & img {
      height: 70px;
      align-self: center;
    }
  }
}
</style>
2
