<template>
  <!-- FLOATING NAV -->
  <div class="floating-nav">
    <button @click="goToSection('home')">Home</button>
    <button @click="goToSection('about')">About</button>
    <button @click="goToSection('guestbook')">Guestbook</button>
  </div>

  <!-- HOME SECTION -->
  <section id="home" class="home">
    <div class="home-card">
      <div class="welcome-text">
        <h1>
          <img class="sticker"
            src="https://supplies.ju.mp/assets/images/gallery05/9747a42c.gif?v=1c1ba870"
            alt="Sticker"
          >
          My Profile
          <img class="sticker"
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
        <button @click="goToSection('guestbook')">Guestbook</button>
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

  <!-- GUESTBOOK -->
  <section id="guestbook" class="content">
    <h2>Guestbook</h2>

    <div class="guestbook">
      <input type="text" placeholder="Your name" disabled>
      <input type="text" placeholder="Your message" disabled>

      <button disabled>Submit</button>

      <p><em>Drop your comments and suggestions!</em></p>
    </div>
  </section>
</template>

<script>
export default {
  name: "Profile",
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
@import "@/css/css-grid.css";
</style>
