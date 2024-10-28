<template>
  <div>
    <header ref="header">
      <nav class="navbar" role="navigation" aria-label="dropdown navigation">
        <div class="navbar-brand">
          <h1 class="title py-3 px-5">Devify</h1>
        </div>
      </nav>
    </header>
    <main ref="main">
      <h1 class="title">Devify</h1>
      <h2 class="subtitle">
        Oopss... sinto muito, a Devify precisou ser retirada do ar
      </h2>
      <p>
        Infelizmente precisei retirar a plataforma do ar. Mas não acabou aqui,
        estou migrando o sistema para uma tecnologia que eu possa dar mais
        suporte. Em breve a Devify estará online novamente :)
      </p>
      <p class="is-flex py-3">
        <a
          href="https://github.com/oGabrielSilva/devify_blog.git"
          target="_blank"
          rel="noopener noreferrer"
        >
          <span class="icon-text">
            <span class="icon">
              <font-awesome-icon :icon="['fab', 'github']" />
            </span>
            <span>Repositório da Devify</span>
          </span>
        </a>
        <a href="mailto:gabriel04gh1.gh@gmail.com">
          <span class="icon-text">
            <span class="icon">
              <font-awesome-icon :icon="['fas', 'envelope']" />
            </span>
            <span>Entrar em contato</span>
          </span>
        </a>
      </p>
      <p class="pt-5 pb-3">
        <img
          src="/devify.png"
          alt="Ícone da Devify"
          aria-label="Ícone do site"
          width="64"
          height="64"
          draggable="false"
        />
      </p>
    </main>
  </div>
</template>

<script setup lang="ts">
import { onMounted, ref } from 'vue'

const header = ref<HTMLElement>()
const main = ref<HTMLElement>()

onMounted(() => {
  if (main.value) {
    main.value.style.minHeight = `calc(95vh - ${header.value?.clientHeight}px)`
  }
})
</script>

<style scoped>
main {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  text-align: center;
  min-height: 50vh;
  padding: 2rem;
}

img {
  width: 64px;
  height: 64px;
}

.is-flex {
  gap: 1rem;
}

@media screen and (max-width: 500px) {
  .is-flex {
    flex-direction: column;
  }
}
</style>
