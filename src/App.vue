<script setup lang="ts">
import AppNav from './components/layout/AppNav.vue'
import AppFooter from './components/layout/AppFooter.vue'
import HeroSection from './components/sections/HeroSection.vue'
import AboutSection from './components/sections/AboutSection.vue'
import SkillsSection from './components/sections/SkillsSection.vue'
import ExperienceSection from './components/sections/ExperienceSection.vue'
// import ProjectsSection from './components/sections/ProjectsSection.vue'
import ContactSection from './components/sections/ContactSection.vue'
import avatarImg from './assets/S__56139782.jpg'

const profile = {
  name: 'Sarawut Duangdee',
  role: 'Back-end Developer | Java Developer',
  email: 'sarawutduangdee@gmail.com',
  phone: '+66-8805-17942',
  location: 'Huai Khwang, Bangkok City, Thailand',
  linkedinUrl: 'https://www.linkedin.com/in/1996-sarawut-duangdee/',
  githubUrl: 'https://github.com/sarawutduangdee'
}

const skills = [
  { label: 'Java', badge: 'J', badgeColor: 'bg-orange-50 text-orange-600' },
  { label: 'Spring Boot', badge: 'SB', badgeColor: 'bg-emerald-50 text-emerald-600' },
  { label: 'TypeScript', badge: 'TS', badgeColor: 'bg-blue-50 text-blue-600' },
  { label: 'Angular', badge: 'NG', badgeColor: 'bg-red-50 text-red-700' },
  { label: 'Oracle SQL', badge: 'SQL', badgeColor: 'bg-red-50 text-red-600' },
  { label: 'Vue', badge: 'V', badgeColor: 'bg-indigo-50 text-indigo-600' },
  { label: 'JavaScript', badge: 'JS', badgeColor: 'bg-yellow-50 text-yellow-600' },
  { label: 'SQL Server', badge: 'MS', badgeColor: 'bg-slate-100 text-slate-700' },
  { label: 'MySQL', badge: 'My', badgeColor: 'bg-blue-50 text-blue-600' },
  { label: 'PostgreSQL', badge: 'PSQL', badgeColor: 'bg-blue-50 text-blue-600' },
  { label: 'MongoDB', badge: 'MDB', badgeColor: 'bg-emerald-50 text-emerald-700' },
  { label: 'Git', badge: 'Git', badgeColor: 'bg-slate-100 text-slate-700' }
  // ,
  // { label: 'C#', badge: 'C#', badgeColor: 'bg-purple-50 text-purple-600' }
]

const experiences = [
  {
    role: 'Java Developer (Contract) · Client: SCB',
    period: 'Oct 2025 — Present',
    company: 'Advanced Systems Consulting (ASC)',
    description: 'Wealth Platform Team: Collaborated on maintenance and development of high-scale wealth management systems. RISS Team: Troubleshooting, bug fixing, and developing new features. Designed robust back-end using Java 17/21 and Spring Boot, RESTful APIs and microservices. Comprehensive Unit Testing for code reliability.'
  },
  {
    role: 'Java Developer (Contract) · Client: TTB',
    period: 'Apr 2025 — Sep 2025',
    company: 'The Prodigy (Thailand) Co., Ltd.',
    description: 'TTB Project: Enhanced business logic, Java Spring Boot modifications, new features, bug fixes. Unit Testing with Spock Framework, BDD approach, full test coverage. Mocking and stubbing for isolated testing.'
  },
  {
    role: 'Java Developer (Contract) · Client: SCB',
    period: 'Sep 2024 — Apr 2025',
    company: 'Extend IT Resource Co., Ltd.',
    description: 'Project Deposit (Fin4U): Microservices architecture with Java 17 and Spring Boot. Integration with external APIs. Account opening condition verification system.'
  },
  {
    role: 'Back-end Developer (Contract) · Client: KTB',
    period: 'Mar 2024 — Aug 2024',
    company: 'The Prodigy (Thailand) Co., Ltd.',
    description: 'E-Solution: Business logic development, Java Spring Boot modifications. PDF and Excel file integration. Comprehensive unit testing for code quality.'
  },
  {
    role: 'Java Developer (Permanent) · Client: AYCAP',
    period: 'Feb 2022 — Mar 2024',
    company: 'PP&P Advance Co., Ltd.',
    description: 'Kbb-eod, Kbb-ucash, Kbb-web, Kbb-service: Maintenance and development, Spring Batch, Spring Cache, unit testing, business logic.'
  },
  {
    role: 'Developer (Permanent)',
    period: 'Mar 2020 — Dec 2021',
    company: 'Baiwa Co., Ltd.',
    description: 'Container Tracking (ITPAC), AOT-RIC, Asset management (Excise Dept), NGMS (Krungsri), Back-office CMS. Jaspersoft Studio for PDF/excel reports, role-based permissions.'
  }
]

// const projects = [
//   {
//     title: 'SkyAnalytics SaaS',
//     description: 'A comprehensive data visualization dashboard for real-time monitoring of cloud infrastructure.',
//     image: 'https://lh3.googleusercontent.com/aida-public/AB6AXuBq6C9XKQeoqFzgKC4pfZgsz1KARtEP5wCrrEUP7T3-H4qKn82hVlMFKmhRBOzM4mvsjrfcBnlMVleAkiZWHAScMhrkxA2EhF9nv8WFN1YdeybTYtstp2DrkrRs2xjYo48CjbmXsjDAikimLlMguec44dQmWNPSRuqm2cyLwvZbg4eHdW6xCfJVJEuFTBJbJTCyCQAYEMYfRpd-GTnrd2fCaefOf3A6t00swBUzstzlW1O1Ps2zrhTtdwPVn2klSmDbPS_d4ITNwxM',
//     tags: [
//       { label: 'Vue 3', color: 'bg-indigo-50 text-indigo-600' },
//       { label: 'Tailwind', color: 'bg-blue-50 text-blue-600' },
//       { label: 'D3.js', color: 'bg-slate-50 text-slate-600' }
//     ]
//   },
//   {
//     title: 'LuxStore Fashion',
//     description: 'High-end headless e-commerce store with seamless Stripe integration and lightning-fast page loads.',
//     image: 'https://lh3.googleusercontent.com/aida-public/AB6AXuAxzid9Y50aSRMU5nqxMKqjFKdnpGiHvPd86XmUFIVN2emAKYeBc-BtDDMs0H8Ml8begvXcLg9-Js1UGMWJthI1LQvO3wP0iRRf4mjWmM2xlY8gkdVDY1y2pMuTOrRhtAhy-e8_rhVtUVpriGYBlFmn7Bf5uPpE8QaNRgUGBryQ64Dj1gITJWPZKjqzTcdc0GxX52zxOOBk_fn0ZL3uosHQJTvkqZAPvKIsXf3qZT7tkQ1_-d7jwhEVdT6Xty5cuz_8JPxDFiJHpzM',
//     tags: [
//       { label: 'Vite', color: 'bg-emerald-50 text-emerald-600' },
//       { label: 'Shopify API', color: 'bg-orange-50 text-orange-600' },
//       { label: 'Pinia', color: 'bg-slate-50 text-slate-600' }
//     ]
//   },
//   {
//     title: 'SyncBoard App',
//     description: 'Real-time collaborative whiteboarding tool for remote teams using WebSockets.',
//     image: 'https://lh3.googleusercontent.com/aida-public/AB6AXuDi-k9wm3KyyYGWA6NyLCnPpB28KsF74CjCldyq02KZZf0Q9GH_Nl9yG0-PQjoqIVogZ3l2_ET68eXmByt83J5dj8YN67x5jRS9DmXL92Za2wsrZ88ATUOx155n5omhfM2QgmJ-ofKgSmrblTKdLC-ZUXG2y8XgislEHJ67UM0Qya9hbiMFByj6OaX5J6W2XImvHNsNeAI35CrMuc2EMG971g3c31Z0i3TeV43b9vkq3tZht9EoiCReVVY5D9T61BpVMeqdSzmh4pw',
//     tags: [
//       { label: 'WebSockets', color: 'bg-purple-50 text-purple-600' },
//       { label: 'Node.js', color: 'bg-red-50 text-red-600' },
//       { label: 'Canvas API', color: 'bg-slate-50 text-slate-600' }
//     ]
//   }
// ]
</script>

<template>
  <div class="bg-slate-50 text-slate-900 antialiased min-h-screen">
    <AppNav />

    <main>
      <HeroSection
        headline="Hi, I'm"
        :highlight="profile.name"
        subheadline="— Back-end Developer | Java Developer"
        description="Bachelor's Degree in Computer Engineering from Suranaree University of Technology. 6 years of experience as a Java Developer, specializing in back-end development with Java Spring Boot and microservices architecture."
        :avatar-src="avatarImg"
        :linkedin-url="profile.linkedinUrl"
        :github-url="profile.githubUrl"
      />
      <AboutSection
        subtitle="Passionate about clean code and building scalable systems."
        :paragraphs="[
          'I am a Bachelor\'s Degree graduate in Computer Engineering from Suranaree University of Technology (2015-2020). With 6 years of experience as a Java Developer, I specialize in back-end development, particularly with Java Spring Boot and microservices architecture.',
          'I have worked with major banks in Thailand including SCB, TTB, KTB, Krungsri, and Excise Department. My focus is on business logic development, RESTful APIs, unit testing (Spock Framework), and integrating PDF/Excel reporting with Jaspersoft Studio.'
        ]"
      />
      <SkillsSection :skills="skills" />
      <ExperienceSection :items="experiences" />
      <!-- <ProjectsSection :projects="projects" /> -->
      <ContactSection
        :email="profile.email"
        :phone="profile.phone"
        :location="profile.location"
      />
    </main>

    <AppFooter
      :copyright="'© 2026 ' + profile.name + '. Built with Vue 3 & Tailwind.'"
      :links="[
        { label: 'LinkedIn', href: profile.linkedinUrl },
        { label: 'GitHub', href: profile.githubUrl }
      ]"
    />
  </div>
</template>
