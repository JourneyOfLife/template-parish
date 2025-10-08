---

# template-parish

This repository hosts the **Journey Of Life** Parish website template—built on Bitrix24 CRM Sites & Stores—to accelerate deployment of GDPR-compliant, multilingual parish sites with service schedules, community engagement, donations, and tenant onboarding.

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [Architecture & Tech Stack](#architecture--tech-stack)  
4. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
   - [Configuration](#configuration)  
   - [Local Development](#local-development)  
5. [Directory Structure](#directory-structure)  
6. [Deployment](#deployment)  
7. [Contributing](#contributing)  
8. [Security & Compliance](#security--compliance)  
9. [License](#license)  
10. [Contact & Support](#contact--support)  

---

## Project Overview

The **template-parish** repository provides a turnkey website template tailored for parishes. It includes global layouts, shared components, and a tenant-onboarding dashboard for Bitrix24 multi-site setups. Designed for parish administrators, it supports service schedules, community news, booking, donations, and staff profiles in Lithuanian, English, and Russian.

---

## Features

- **Key Pages**  
  - Home with hero value prop and CTA  
  - Service Schedule & Calendar  
  - Community News & Announcements  
  - Secure Donation & E-Giving  
  - Booking & Consultation Form  
  - Photo Gallery & Events Recap  
  - Staff & Volunteer Profiles  
  - FAQ & Support Center  
  - Contact & Location (Google Maps)  

- **Core Modules**  
  - Donation / Online Giving via Bitrix24 CRM  
  - Event Scheduling / Calendar Integration  
  - Blog / News Feed  
  - Image Gallery & Media Carousel  
  - Staff Profiles & Roles  
  - Social Media Integration  
  - Testimonials & Community Feedback  
  - Multilingual Switcher (LT/EN/RU)  

- **Design & Branding**  
  - Colors: Deep Blue (#1A237E), Gold (#FFD700), White (#FFFFFF)  
  - Typography: Montserrat (headings), Roboto (body)  
  - SVG iconography with warm-tone photography  

---

## Architecture & Tech Stack

| Layer                  | Technology                                    |
|------------------------|-----------------------------------------------|
| Frontend               | Bitrix24 Site Builder, Semantic HTML5, SASS   |
| Shared Components      | SASS variables, SVG icon library              |
| CMS                    | 1C-Bitrix Multi-Site                          |
| CRM & E-Commerce       | Bitrix24 CRM Online Store Enterprise          |
| Middleware (optional)  | Django REST Framework, API Gateway            |
| Database               | PostgreSQL (structured), MongoDB (analytics)  |
| CI/CD                  | GitHub Actions, Docker                        |
| Hosting                | Linux Home Server / Google Cloud (hybrid)     |
| Containerization       | Kubernetes (optional scaling)                 |

---

## Getting Started

### Prerequisites

- Git 2.20+  
- Node.js 14+ & npm or Yarn  
- Access to Bitrix24 Sites & CRM modules  
- Docker (optional for local containers)  

### Installation

```bash
git clone https://github.com/JourneyOfLife/template-parish.git
cd template-parish
npm install          # or yarn install
```

### Configuration

1. Copy `.env.example` to `.env`  
2. Populate environment variables:
   ```
   BITRIX24_WEBHOOK_URL=
   TEMPLATE_ID=PARISH
   DEFAULT_LANGUAGE=lt
   ```
3. Import the template ZIP via Bitrix24 Sites admin and map pages.

### Local Development

```bash
npm run dev
```

Preview at `http://localhost:3000`. Customize SASS in `src/styles/variables.scss`.

---

## Directory Structure

```
/
├── .github/                  # CI/CD workflows
├── src/
│   ├── pages/                # Page templates (home, schedule, news...)
│   ├── components/           # Shared UI components
│   ├── styles/               # SASS partials, variables, mixins
│   └── assets/               # Images, SVG icons
├── .env.example
├── package.json
└── docker-compose.yml        # Optional local containers
```

---

## Deployment

1. Build production assets:
   ```bash
   npm run build
   ```
2. Package as a Bitrix24-compatible ZIP file.  
3. Import via Bitrix24 Sites → Templates → Import.  
4. Assign to parish tenant subdomain.

---

## Contributing

1. Fork this repository  
2. Create a feature branch:
   ```bash
   git checkout -b feature/XYZ
   ```
3. Commit changes with clear messages  
4. Push branch and open a Pull Request  
5. Ensure all CI checks pass  

Refer to [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines.

---

## Security & Compliance

- GDPR-compliant data handling and privacy notices  
- Cookie banner & Privacy Policy via Bitrix modules  
- Role-based access control enforced in frontend and backend  
- Regular dependency vulnerability scans

---

## License

This template is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

## Contact & Support

For assistance or questions:

- **Lead Architect:** Gintaras Kazlauskas  
- **Email:** gintaras.kazlauskas@gyvenimo-kelias.lt  
- **GitHub Issues:** https://github.com/JourneyOfLife/template-parish/issues
