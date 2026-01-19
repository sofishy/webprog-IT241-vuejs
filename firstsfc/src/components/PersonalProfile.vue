<template>
  <!-- FLOATING NAV -->
  <div class="floating-nav">
    <button @click="goToSection('home')">Home</button>
    <button @click="goToSection('about')">About</button>
  </div>

  <!-- HOME SECTION -->
  <section id="home" class="home">
    <div class="home-card">
      <div class="welcome-text">
        <h1>
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
        <button @click="goToResources">Resources</button>
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
    },
    goToResources() {
      window.location.href = "resources.html"
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
  background: #fde2e4;
  color: #5a3a2e;
  text-align: center;
}

/* ---------------- FLOATING NAV ---------------- */
.floating-nav {
  position: fixed;
  top: 20px;
  right: 20px;
  z-index: 1000;
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 12px;
  border-radius: 20px;
  background: #f3d6c6;
  border: 2px solid #d2b8a3;
  box-shadow: 0 8px 20px rgba(0,0,0,0.15);
}

.floating-nav button {
  background: #e89bb0;
  border: none;
  color: white;
  padding: 10px 14px;
  border-radius: 15px;
  cursor: pointer;
  font-weight: 600;
}

.floating-nav button:hover {
  opacity: 0.85;
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

/* ---------------- WELCOME TEXT ---------------- */
.welcome-text h1 {
  color: #e89bb0;
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.sticker {
  width: 40px;
  vertical-align: middle;
}

.tagline {
  font-size: 1.1rem;
  margin-bottom: 20px;
}

/* ---------------- MENU BUTTONS ---------------- */
.menu {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 10px;
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

/* ---------------- MEDIA QUERIES ---------------- */
@media (max-width: 768px) {
  .home-card {
    padding: 20px;
  }
}
</style>
