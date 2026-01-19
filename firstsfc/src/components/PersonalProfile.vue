<template>
  <!-- HOME SECTION -->
  <section id="home" class="home">
    <div class="home-card">
      <div class="welcome-text">
        <h1 class="title-center">
          <img
            class="sticker"
            src="https://supplies.ju.mp/assets/images/gallery05/9747a42c.gif?v=1c1ba870"
            alt="Sticker"
          >
          My Profile
          <img
            class="sticker"
            src="https://supplies.ju.mp/assets/images/gallery05/9747a42c.gif?v=1c1ba870"
            alt="Sticker"
          >
        </h1>

        <p class="tagline">
          Welcome to Sofishy's web!
        </p>
      </div>

      <div class="menu">
        <button @click="goToSection('about')">About Me</button>
      </div>
    </div>
  </section>

  <!-- ABOUT SECTION -->
  <section id="about" class="content">
    <h2>About Me</h2>
    <p>I am Iane Sofia Francheska Padua, an IT student at Asia Pacific College.</p>

    <h2>Education / Achievements</h2>
    <p>
      Graduated from Pasay City South High School<br>
      Graduated with High Honors<br>
      Top 4 Best Capstone Project<br>
      Best Research Group in Physical Science
    </p>

    <h2>IT Experience</h2>
    <p>
      Python Programming<br>
      Basic Networking<br>
      UI / UX Designing
    </p>

    <h2>Hobbies & Interests</h2>
    <p>
      Watching sitcoms and dramas<br>
      Playing instruments<br>
      Crocheting
    </p>

    <h2>Goals in Life</h2>
    <p>
      My goal is to become successful in the IT field and build a stable future.
    </p>
  </section>
</template>

<script>
export default {
  name: "PersonalProfile",
  methods: {
    goToSection(id) {
      const section = document.getElementById(id)
      if (section) {
        section.scrollIntoView({ behavior: "smooth" })
      }
    }
  }
}
</script>

<style scoped>
/* ---------------- GLOBAL ---------------- */
* {
  box-sizing: border-box;
  font-family: "Segoe UI", Arial, sans-serif;
}

body {
  margin: 0;
  background: #fde2e4; /* PINK BACKGROUND (from your CSS) */
  color: #5a3a2e;
  text-align: center;
}

/* ---------------- HOME ---------------- */
.home {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.home-card {
  background: #fff7f2;
  padding: 40px;
  max-width: 700px;
  width: 90%;
  border-radius: 24px;
  border: 2px solid #d2b8a3;
  box-shadow: 0 10px 25px rgba(0,0,0,0.15);
}

/* ---------------- TITLE ---------------- */
.title-center {
  text-align: center;
  color: #e89bb0;
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.sticker {
  width: 40px;
  vertical-align: middle;
}

/* ---------------- TEXT ---------------- */
.tagline {
  font-size: 1.1rem;
  margin-bottom: 20px;
}

/* ---------------- MENU ---------------- */
.menu {
  display: flex;
  justify-content: center;
}

.menu button {
  background: #f4a6b8;
  color: white;
  border: none;
  padding: 10px 18px;
  border-radius: 20px;
  font-weight: 600;
  cursor: pointer;
}

.menu button:hover {
  opacity: 0.85;
}

/* ---------------- CONTENT ---------------- */
.content {
  padding: 60px 15px;
}

.content h2 {
  color: #e89bb0;
  margin-top: 50px;
  text-decoration: underline;
}

.content p {
  background: #fff7f2;
  padding: 15px;
  margin: 20px auto;
  max-width: 800px;
  border-radius: 14px;
  border: 2px solid #d2b8a3;
}

/* ---------------- RESPONSIVE ---------------- */
@media (max-width: 768px) {
  .home-card {
    padding: 20px;
  }
}
</style>
