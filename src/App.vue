<script setup lang="ts">
import './global.css'
</script>

<template>
  <div class="container">
    <header>
      <i class="ph-cat"></i>
      <h2>Converse com a Uko</h2>
    </header>

    <main></main>

    <footer>
      <form action="index.html" method="post">
        <textarea name="message" id="message" placeholder="Digite sua mensagem..."></textarea>
        <button type="submit" id="send">
          <i class="ph-paper-plane-right-fill"></i>
        </button>
      </form>
    </footer>
  </div>
</template>

<style scoped>
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;

    width: 33%;
    margin: auto;
    padding: 1rem 1.5rem;

    border: 2px solid;
    border-radius: 8px;
  }

  header {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 1rem 0;
    margin-bottom: 2rem;

    border-bottom: 2px solid;
  }

  header i {
    font-size: 1.5rem;
  }

  main {
    display: flex;
    flex-direction: column;
    gap: 2rem;
    max-height: 433px;
    overflow-y: scroll;

    padding: 2rem 1rem 2rem 0;
  }

  .received {
    word-break: break-all;
    position: relative;

    border: 2px solid;
    border-radius: 0 8px 8px 8px;
    padding: 0.875rem 1rem;

    margin-right: 30%;
  }

  .received::before {
    content: 'Uko diz:';
    position: absolute;
    top: 0;
    left: 0;
    margin-top: -24px;
  }

  .sent {
    word-break: break-all;
    position: relative;

    border: 2px solid;
    border-radius: 8px 0px 8px 8px;
    padding: 0.875rem 1rem;
    
    margin-left: 30%;
  }

  .sent::before {
    content: 'Você diz:';
    position: absolute;
    top: 0;
    right: 0;
    margin-top: -24px;
  }

  footer form {
    width: 100%;
    display: flex;
    align-items: center;
    gap: 10px;
  }

  textarea {
    width: 100%;
    resize: none;
    color: #E1E1E6;
    background-color: transparent;

    padding: 0.5rem 0.5rem 0 0.5rem;
    height: 3rem;

    border-radius: 6px;

    cursor: auto;
  }

  textarea::-webkit-scrollbar-thumb, main::-webkit-scrollbar-thumb {
    background: rgb(235, 211, 0); 
    border-radius: 10px;
  }

  ::-webkit-scrollbar-thumb:hover {
    background: rgb(190, 172, 1);
  }

  ::-webkit-scrollbar {
    width: 6px;
  }

  ::-webkit-scrollbar-track {
    width: 20px;
  }

  footer button {
    display: flex;
    padding: 1rem;
    background: rgb(235, 211, 0);
    border: none;
    border-radius: 50%;

    cursor: pointer;
  }

  footer button:active {
    transition: background 0.2s;
    background: rgb(226, 195, 17);
  }

  footer button:hover {
    transition: background 0.2s;
    background: rgb(226, 195, 17);
  }

  footer button i {
    font-size: 1.3rem;
  }
</style>
