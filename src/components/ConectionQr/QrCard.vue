<template>
  <section>
    <div class="container">
      <div class="text">
        <h2>Conecta tu cuenta de WhatsApp</h2>
        <p>Envia mesajes privavos a tus clientes a traves de la App</p>

        <ol>
          <li></li>
          <li></li>
          <li></li>
          <li></li>
        </ol>
      </div>
      <div class="qr-code"></div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #fcf9f6;

  .container {
    font-family: 'Roboto Flex', sans-serif;
    display: flex;
    flex-direction: column;
    background-color: #ffffff;
    padding: 20px;
    border: 1px solid black;
    border-radius: 1.8rem;
    width: 90%;
    height: 80%;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);

    h2 {
      font-size: 2.4rem;
      font-weight: 400;
    }
  }
}
</style>
