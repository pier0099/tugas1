<template>
  <div class="cv">
    <header>
      <h1>{{ name }}</h1>
      <p>{{ title }}</p>
    </header>
    <section>
      <h2>Tentang Saya</h2>
      <p>{{ about }}</p>
    </section>
    <section>
      <h2>Pengalaman</h2>
      <ul>
        <li v-for="experience in experiences" :key="experience.id">
          <h3>{{ experience.position }}</h3>
          <p>{{ experience.company }} - {{ experience.years }}</p>
        </li>
      </ul>
    </section>
    <section>
      <h2>Proyek</h2>
      <ul>
        <li v-for="project in projects" :key="project.id">
          <h3>{{ project.name }}</h3>
          <p>{{ project.description }}</p>
        </li>
      </ul>
    </section>
    <section>
      <h2>Kontak</h2>
      <p>Email: {{ email }}</p>
      <p>Telepon: {{ phone }}</p>
    </section>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      name: "Fiere Maulana",
      title: "CEO",
      about: "Mystery",
      experiences: [
        { id: 1, position: "OB", company: "Perusahaan pak saipul", years: "2019-2021" },
        { id: 2, position: "CEO", company: "Perusahaan Microsoft", years: "2021-2024" }
      ],
      projects: [
        { id: 1, name: "Proyek 1", description: "Deskripsi proyek 1" },
        { id: 2, name: "Proyek 2", description: "Deskripsi proyek 2" }
      ],
      email: "email@example.com",
      phone: "08123456789"
    };
  }
};
</script>

<style scoped>
.cv {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  padding: 2rem;
}
header {
  padding: 2rem;
  background-color: #f5f5f5;
}
h1 {
  margin: 0;
  font-size: 2.5rem;
}
p {
  font-size: 1.2rem;
  color: #555;
}
section {
  padding: 2rem;
  text-align: left;
}
h2 {
  font-size: 2rem;
  margin-bottom: 1rem;
}
ul {
  list-style: none;
  padding: 0;
}
li {
  margin-bottom: 1rem;
}
h3 {
  margin: 0;
  font-size: 1.2rem;
}
p {
  margin: 0;
  font-size: 1rem;
  color: #1f1a80;
}
</style>
