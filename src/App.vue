<template>
  <div class="app">
    <Nav />

    <hr class="divider" />

    <!-- 欢迎区 -->
    <section id="home" class="home">
      <h2>Welcome to Pdnode Team</h2>
      <p>A group of people with similar interests.</p>
    </section>

    <!-- About -->
    <section id="about" class="about">
      <h2>About Us</h2>
      <p>
        Pdnode is a group of people with the same interests. Founded on
        2024-07-10.
      </p>
      <p>Note: We are not a company, just an organization.</p>
    </section>

    <!-- Team Members -->
    <section id="members" class="members">
      <h2>Our Team Members</h2>
      <div class="members-grid">
        <div v-for="member in teamMembers" :key="member.name" class="card">
          <h3>{{ member.name }}</h3>
          <p><strong>Joined:</strong> {{ member.joined }}</p>
          <p><strong>Position:</strong> {{ member.position }}</p>
          <p><strong>Main tasks:</strong> {{ member.mainTasks }}</p>
          <p class="intro">{{ member.introduce }}</p>
        </div>
      </div>
    </section>

    <!-- Services -->
    <section id="services" class="services">
      <h2>Services</h2>
      <ul>
        <li v-for="service in services" :key="service">{{ service }}</li>
      </ul>
    </section>

    <!-- Contact -->
    <section id="contact" class="contact">
      <h2>Contact Us</h2>
      <p><strong>Email:</strong> contact@pdnode.com</p>
      <p>
        <strong>Github Issues:</strong>
        <a href="https://github.com/BretRen/pdnode/issues">Here</a>
      </p>
    </section>

    <!-- Footer -->
    <footer class="footer">
      © 2025 Pdnode. All rights reserved. ·
      <a href="https://forum.pdnode.com/d/5-pdnode-terms-of-service">Terms</a> ·
      <a href="https://forum.pdnode.com/d/6-pdnode-privacy-policy">Privacy</a>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Nav from './components/Nav.vue'

const teamMembers = ref([
  {
    name: "Bret",
    joined: "2024-07-10",
    position: "Founder",
    mainTasks: "Full-stack Development",
    introduce: "Responsible for the main development of Pdnode.",
  },
  {
    name: "Mark",
    joined: "Unknown",
    position: "Admin",
    mainTasks: "Front-end Development",
    introduce: "Focus on front-end development of Nextjs and Mui+react.",
  },
  {
    name: "owg",
    joined: "2025-07-01",
    position: "Member",
    mainTasks: "Pdnode MC Management",
    introduce: "Responsible for the management and maintenance of Pdnode MC.",
  },
])

const services = ref(["ChatRoom", "Website Development"])
</script>

<style scoped>
/* App */
.app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  font-family: sans-serif;
  color: #333;
}

/* Divider */
.divider {
  height: 1px;
  background: #ccc;
  border: none;
  width: 100%;
}

/* Sections */
section {
  padding: 4rem 1rem;
}

section h2 {
  font-size: 2rem;
  font-weight: bold;
  color: #2563eb;
  margin-bottom: 1rem;
}

/* Home */
.home {
  text-align: center;
  background: #f9fafb;
}

.home h2 {
  font-size: 2.5rem;
}

.home p {
  font-size: 1.2rem;
  color: #555;
}

/* About */
.about {
  background: #fff;
  color: #444;
}

/* Team Members */
.members {
  background: #f9fafb;
}

.members-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1.5rem;
}

@media (min-width: 640px) {
  .members-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 768px) {
  .members-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

.card {
  background: #fff;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  transition: 0.2s;
}

.card:hover {
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.15);
}

.card h3 {
  font-size: 1.25rem;
  margin-bottom: 0.5rem;
}

.card p {
  margin: 0.3rem 0;
  color: #555;
  font-size: 0.9rem;
}

.intro {
  margin-top: 0.5rem;
  color: #333;
}

/* Services */
.services ul {
  list-style: disc inside;
  max-width: 600px;
  margin: 0 auto;
  color: #444;
}

.services li {
  margin: 0.5rem 0;
}

/* Contact */
.contact {
  background: #f9fafb;
}

.contact a {
  color: #2563eb;
  text-decoration: none;
}

.contact a:hover {
  text-decoration: underline;
}

/* Footer */
.footer {
  padding: 1.5rem;
  background: #fff;
  border-top: 1px solid #ddd;
  font-size: 0.9rem;
  color: #666;
  text-align: center;
}

.footer a {
  color: #2563eb;
  text-decoration: none;
}

.footer a:hover {
  text-decoration: underline;
}
</style>
