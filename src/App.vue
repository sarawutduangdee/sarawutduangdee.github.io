<script setup lang="ts">
import AppNav from './components/layout/AppNav.vue'
import AppFooter from './components/layout/AppFooter.vue'
import HeroSection from './components/sections/HeroSection.vue'
import AboutSection from './components/sections/AboutSection.vue'
import SkillsSection from './components/sections/SkillsSection.vue'
import ExperienceSection from './components/sections/ExperienceSection.vue'
import ContactSection from './components/sections/ContactSection.vue'
import avatarImg from './assets/S__56139782.jpg'

const profile = {
  name: 'Sarawut Duangdee',
  role: 'Back-end Developer | Java Developer | Full Stack Developer',
  email: 'sarawutduangdee@gmail.com',
  phone: '+66-8805-17942',
  location: 'Huai Khwang, Bangkok City, Thailand',
  linkedinUrl: 'https://www.linkedin.com/in/1996-sarawut-duangdee/',
  githubUrl: 'https://github.com/sarawutduangdee'
}

const skills = [
  { label: 'Java', badgeColor: 'bg-orange-50 text-orange-600' },
  { label: 'Spring Boot', badgeColor: 'bg-emerald-50 text-emerald-600' },
  { label: 'TypeScript', badgeColor: 'bg-blue-50 text-blue-600' },
  { label: 'Angular', badgeColor: 'bg-red-50 text-red-700' },
  { label: 'Oracle SQL', badgeColor: 'bg-rose-50 text-rose-600' },
  { label: 'Vue', badgeColor: 'bg-indigo-50 text-indigo-600' },
  { label: 'JavaScript', badgeColor: 'bg-yellow-50 text-yellow-600' },
  { label: 'SQL Server', badgeColor: 'bg-slate-100 text-slate-700' },
  { label: 'MySQL', badgeColor: 'bg-cyan-50 text-cyan-700' },
  { label: 'PostgreSQL', badgeColor: 'bg-blue-50 text-blue-800' },
  { label: 'MongoDB', badgeColor: 'bg-emerald-50 text-emerald-700' },
  { label: 'Git', badgeColor: 'bg-slate-100 text-slate-700' },
  { label: 'Docker', badgeColor: 'bg-sky-50 text-sky-600' },
  { label: 'Vite', badgeColor: 'bg-violet-50 text-violet-600' }
]

const experiences = [
  {
    role: 'Back-end Developer (Contract) · Client: AIS',
    period: 'Aug 2026 — Present',
    company: 'PE Resourcing Service Co.,Ltd.',
    description:
      'Contract back-end developer for AIS: Java Spring Boot services, business-logic changes, new features, and defect fixes with the client team.',
    highlights: [
      'Enhance and adjust business rules in existing Spring Boot services to match AIS requirements.',
      'Implement new features and REST API updates, then fix UAT/production defects.',
      'Write and maintain unit tests so core flows stay reliable after each change.',
      'Collaborate with AIS stakeholders to clarify requirements before releasing logic updates.'
    ]
  },
  {
    role: 'Back-end Developer (Contract) · Client: KTB',
    period: 'Mar 2026 — Jul 2026',
    company: 'Azure Computers (Thailand) Co., Ltd.',
    description:
      'Project LEXS for Krungthai Bank: joined as a back-end developer to extend Java Spring Boot services used in the legal-execution domain.',
    highlights: [
      'Analyze existing business logic and apply Spring Boot changes for new requirements.',
      'Deliver feature work and bug fixes on service APIs used by LEXS workflows.',
      'Add unit tests around changed modules to reduce regression risk.'
    ]
  },
  {
    role: 'Java Developer (Contract) · Client: SCB',
    period: 'Oct 2025 — Mar 2026',
    company: 'Advanced Systems Consulting (ASC)',
    description:
      'Supported two SCB teams — Wealth Platform and RISS — on high-scale Java back-end systems for wealth and related banking services.',
    highlights: [
      'Wealth Platform: maintain and develop services for large-scale wealth management, including ongoing change requests.',
      'RISS: troubleshoot incidents, fix defects, and implement new features under bank delivery cycles.',
      'Design and extend back-end APIs with Java 17/21, Spring Boot, RESTful services, and a microservices style.',
      'Raise reliability with comprehensive unit tests before promoting code to higher environments.'
    ]
  },
  {
    role: 'Java Developer (Contract) · Client: TTB',
    period: 'Apr 2025 — Sep 2025',
    company: 'The Prodigy (Thailand) Co., Ltd.',
    description:
      'TTB banking project: back-end work on Java Spring Boot services, focused on business-rule changes and testable delivery.',
    highlights: [
      'Enhance business logic, add features, and patch defects in Spring Boot services.',
      'Practice BDD-style unit testing with the Spock Framework, aiming for strong coverage on changed flows.',
      'Use mocking and stubbing to isolate services and verify edge cases without depending on live systems.'
    ]
  },
  {
    role: 'Java Developer (Contract) · Client: SCB',
    period: 'Sep 2024 — Apr 2025',
    company: 'Extend IT Resource Co., Ltd.',
    description:
      'Project Deposit (Fin4U): Java 17 / Spring Boot microservices for deposit and account-opening journeys.',
    highlights: [
      'Build and maintain microservices that support deposit/account flows on Fin4U.',
      'Integrate with external bank APIs and handle request/response mapping and error cases.',
      'Implement account-opening condition checks so eligibility rules are enforced in the back-end.'
    ]
  },
  {
    role: 'Back-end Developer (Contract) · Client: KTB',
    period: 'Mar 2024 — Aug 2024',
    company: 'The Prodigy (Thailand) Co., Ltd.',
    description:
      'E-Solution for Krungthai Bank: Spring Boot back-end for business processes that also produce PDF and Excel outputs.',
    highlights: [
      'Develop and adjust business logic in Java Spring Boot modules used by E-Solution.',
      'Integrate PDF and Excel generation/export into existing service flows.',
      'Add unit tests around report and business paths to keep delivery quality consistent.'
    ]
  },
  {
    role: 'Java Developer (Permanent) · Client: AYCAP',
    period: 'Feb 2022 — Mar 2024',
    company: 'PP&P Advance Co., Ltd.',
    description:
      'Long-term ownership of AYCAP Kbb systems (Kbb-eod, Kbb-ucash, Kbb-web, Kbb-service): maintenance, batch jobs, and day-to-day business logic.',
    highlights: [
      'Maintain and develop Kbb-eod, Kbb-ucash, Kbb-web, and Kbb-service across 2+ years.',
      'Implement and tune Spring Batch jobs for end-of-day and related processing.',
      'Apply Spring Cache where it helps reduce load on frequently used data.',
      'Cover business-rule changes with unit tests and coordinate with the client on production issues.'
    ]
  },
  {
    role: 'Developer (Permanent)',
    period: 'Mar 2020 — Dec 2021',
    company: 'Baiwa Co., Ltd.',
    description:
      'Full-stack style delivery across government and financial projects: tracking, asset, CMS, and reporting systems.',
    highlights: [
      'Container Tracking (ITPAC) and AOT-RIC: application features for tracking and related operations.',
      'Asset management for the Excise Department: CRUD flows and permission-aware screens/services.',
      'NGMS (Krungsri) and back-office CMS: feature work with role-based access control.',
      'Design PDF/Excel reports in Jaspersoft Studio and wire them into application workflows.'
    ]
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
        :subheadline="profile.role"
        cta-href="#experience"
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
