# Cotyledon Lab - Business Landing Page

A modern, static business landing page built with Astro and Tailwind CSS. Features include a hero section, features showcase, contact form, SEO optimization, and Docker deployment.

## 🚀 Features

- **Hero Section**: Eye-catching landing area with call-to-action buttons
- **Features Grid**: Showcase your business capabilities with icon-based cards
- **Contact Form**: Integrated form with placeholder API for lead collection
- **SEO Optimized**: Built-in meta tags, Open Graph, and Twitter Cards
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Fast Performance**: Static site generation for optimal loading speeds
- **Docker Ready**: Multi-stage Dockerfile for production deployment

## 📁 Project Structure

```
/
├── public/
│   ├── favicon.svg         # Site favicon
│   └── social-image.jpg    # Open Graph/Twitter image
├── src/
│   ├── components/
│   │   ├── Hero.astro      # Hero section
│   │   ├── Features.astro  # Features grid
│   │   └── ContactForm.astro # Contact form with placeholder API
│   ├── layouts/
│   │   └── BaseLayout.astro # Base layout with SEO meta tags
│   ├── pages/
│   │   └── index.astro     # Home page
│   └── config.ts           # Site configuration and metadata
├── astro.config.mjs        # Astro configuration
├── tailwind.config.mjs     # Tailwind CSS configuration
├── tsconfig.json           # TypeScript configuration
├── Dockerfile              # Multi-stage Docker build
├── .dockerignore           # Docker ignore rules
└── package.json            # Dependencies and scripts
```

## 🛠️ Prerequisites

- Node.js 18+ and npm
- Docker (for containerized deployment)

## 📦 Installation

1. Clone the repository:
```bash
git clone https://github.com/cotyledonlab/cotyledonlab.com.git
cd cotyledonlab.com
```

2. Install dependencies:
```bash
npm install
```

## 🧞 Commands

All commands are run from the root of the project:

| Command                   | Action                                           |
| :------------------------ | :----------------------------------------------- |
| `npm install`             | Installs dependencies                            |
| `npm run dev`             | Starts local dev server at `localhost:4321`      |
| `npm run build`           | Build your production site to `./dist/`          |
| `npm run preview`         | Preview your build locally, before deploying     |
| `npm run astro`           | Run CLI commands like `astro add`, `astro check` |

## 🐳 Docker Deployment

### Build Docker Image

```bash
docker build -t cotyledonlab-landing .
```

### Run Docker Container

```bash
docker run -d -p 8080:80 --name cotyledonlab cotyledonlab-landing
```

The site will be available at `http://localhost:8080`

### Stop Container

```bash
docker stop cotyledonlab
docker rm cotyledonlab
```

## ⚙️ Configuration

Edit `src/config.ts` to customize site metadata:

```typescript
export const SITE_CONFIG = {
  title: 'Your Company Name',
  description: 'Your company description',
  url: 'https://yoursite.com',
  image: '/social-image.jpg',
  author: 'Your Team',
  email: 'contact@yoursite.com',
  twitter: '@yourhandle',
  keywords: 'your, keywords, here',
};
```

## 🎨 Customization

- **Colors**: Modify Tailwind colors in `tailwind.config.mjs`
- **Content**: Edit component files in `src/components/`
- **Styling**: Use Tailwind utility classes throughout
- **Features**: Update feature list in `src/components/Features.astro`
- **Contact API**: Replace placeholder API in `src/components/ContactForm.astro` with your backend endpoint

## 📝 Contact Form Integration

The contact form includes a placeholder API. To integrate with a real backend:

1. Replace the simulated API call in `src/components/ContactForm.astro`:
```javascript
const response = await fetch('/api/contact', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify(data),
});
```

2. Set up your backend endpoint to handle form submissions
3. Update error handling as needed

## 🌐 Deployment

The built static files in `dist/` can be deployed to any static hosting service:

- **Netlify**: Connect your repository and deploy
- **Vercel**: Import your Git repository
- **GitHub Pages**: Use GitHub Actions for deployment
- **Docker/Kubernetes**: Use the provided Dockerfile
- **Traditional hosting**: Upload `dist/` contents via FTP/SFTP

## 📄 License

MIT

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!
