<template>
  <header>
    <nav class="container">
      <div>
        <img src="../assets/img/logo-futura-dark.svg" alt="Logo de Futura" />
      </div>
      <div>
        <ul>
          <li>
            <a href="#">SCIENCES<font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
          </li>
          <li>
            <a href="#">SANTE<font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
          </li>
          <li>
            <a href="#">TECH<font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
          </li>
          <li>
            <a href="#">MAISON<font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
          </li>
          <li>
            <a href="#">PLANETE<font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
          </li>
        </ul>
      </div>
      <div>
        <button>JE M'ABONNE</button>
      </div>
    </nav>
  </header>
</template>

<style scoped>
header {
  background: linear-gradient(0.25turn, var(--light-purple), var(--dark-purple));
  height: 50px;
  display: flex;
  align-items: center;
  justify-content: center;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

ul {
  display: flex;
  gap: 45px;
}

li a {
  display: flex;
  gap: 10px;
  align-items: center;
}

svg {
  font-size: 12px;
}

button {
  background-color: #ffb00d;
  padding: 10px 15px;
  border: none;
  color: white;
}
</style>
