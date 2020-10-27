<template>
  <div id="app">
    <header class="header">
      <div class="brand">
        <div class="brand_logo">
          <img src="" alt="" />
        </div>
        <div class="brand_brand">
          {{ brand }}
        </div>
      </div>

      <nav>
        <ul>
          <li v-for="(item, i) in menuItems" :key="i">
            {{ item.label }}
          </li>
        </ul>
      </nav>
    </header>

    <div class="container">
      <div class="sideBar"></div>
      <div class="content_cards">
        <div class="profile">
          <img class="profile_img" src="./assets/profile.jpg" alt="profile" />
          <div class="buttons-container">
            <button>
              <img src="./assets/folder.png" alt="icon-folder" /><span
                >TUS DATOS</span
              >
            </button>
            <button>
              <img src="./assets/ID.png" alt="icon-folder" /><span
                >CARNÉ DIGITAL</span
              >
            </button>
          </div>
          <div class="profile_data">
            <div class="profile-content">
              <h4>Cédula</h4>
              <p>1.020.489.987</p>
            </div>

            <div class="profile-content">
              <h4>Tipo de Usuario</h4>
              <p>Aguila</p>
            </div>

            <div class="profile-content">
              <h4>Celular</h4>
              <p>310 290 39 38</p>
            </div>
            <div class="profile-content">
              <h4>Correo</h4>
              <p>andrea.tovar@ab-inbev.com</p>
            </div>
          </div>
        </div>
        <div class="contacts">
          <div class="contacts_header">
            <div class="title_contacts">
              <img src="./assets/contacts.png" alt="">
              <span>TUS CONTACTOS</span>
            </div>
            <div class="seeAll_contacts">
              <a href="#"> Ver Todos</a>
            </div>

          </div>
          <div class="contacts-people">
              <ul>
                <li>
                  <img src="./assets/add.jpg" alt="">
                  <span>Agregar</span>
                </li>
                <li>
                  <img src="./assets/people1.png" alt="">
                  <span>Line Manager</span>
                </li>
                <li>
                  <img src="./assets/people1.png" alt="">
                  <span>Line Manager</span>
                </li>
                <li>
                  <img src="./assets/people1.png" alt="">
                  <span>Line Manager</span>
                </li>
                <li>
                  <img src="./assets/people1.png" alt="">
                  <span>Line Manager</span>
                </li>
                <li>
                  <img src="./assets/people1.png" alt="">
                  <span>Line Manager</span>
                </li>
                <li>
                  <img src="./assets/people1.png" alt="">
                  <span>Line Manager</span>
                </li>
                <li>
                  <img src="./assets/people1.png" alt="">
                  <span>Line Manager</span>
                </li>
              </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      brand: "EMBAJADORES",
      menuItems: [
        { label: "Universo cervecero" },
        { label: "Cuidados y beneficios" },
        { label: "Un mundo mejor" },
        { label: "¿Qué es BeerOffice" },
      ],
    };
  },
};
</script>

<style>
body {
  margin: 0;
}
.header {
  display: flex;
  justify-content: space-between;
  padding: 1rem;
  box-shadow: 0 4px 2px -2px gray;
  z-index: 1000;
  position: relative;
}

.brand {
  color: #d82a2a;
  font-weight: 700;
  font-size: 1.4rem;
  display: flex;
}

ul {
  list-style: none;
  display: flex;
}
li {
  margin-left: 15px;
}

.container {
  display: grid;
  grid-template-columns: 1fr 12fr;
  grid-template-rows: 1fr;
  gap: 0;
  grid-template-areas: "sideBar content_cards";
  height: 100vh;
}

.sideBar {
  grid-area: sideBar;
  background: #f2f3f2;
}

.content_cards {
  grid-area: content_cards;
  background: white;
  padding: 1rem;
  display: grid;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: 0.5fr 1fr 1fr;
  gap: 20px;
  grid-template-areas:
    "profile contacts"
    "profile ."
    "profile .";
}

.profile {
  grid-area: profile;
  border: 1px solid gray;
  border-radius: 15px;
  margin-bottom: 1rem;
}

.profile_img {
  width: 100%;
  object-fit: cover;
  border-radius: 15px;
}
.contacts {
  grid-area: contacts;
  border: 1px solid gray;
  border-radius: 15px;
}

.buttons-container {
  margin-top: 1rem;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

button {
  border: 1px solid gray;
  border-radius: 25px;
  padding: 0.4rem 1.2rem;
  background: white;
  display: flex;
  justify-content: center;
  align-items: center;
}

button > img {
  margin-right: 4px;
}
button:hover {
  background: #d82a2a;
  color: white;
}
button:focus {
  outline: none;
}

.profile_data {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}

.profile-content {
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;
}

.profile-content > h4 {
  margin-bottom: 0;
}
.profile-content > p {
  margin-top: 0;
}
.contacts_header{
  display: flex;
  justify-content: space-between;
  padding: 1rem;
}
.title_contacts{
  display: flex;
  justify-content: center;
  align-items: center;
}
.seeAll_contacts > a {
  color: black;
  font-weight: 700;
}

.contacts-people > ul > li {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 0 15px;
}



</style>
