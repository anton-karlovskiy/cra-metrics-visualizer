# CRA Metrics Visualizer - Lighthouse Performance Analysis Tool

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![React](https://img.shields.io/badge/React-16.13.1-blue.svg)](https://reactjs.org/)
[![Lighthouse](https://img.shields.io/badge/Lighthouse-6.0.0-orange.svg)](https://developers.google.com/web/tools/lighthouse)
[![Node.js](https://img.shields.io/badge/Node.js-Express-green.svg)](https://nodejs.org/)

## 🚀 Overview

**CRA Metrics Visualizer** is a powerful web performance analysis tool that provides comprehensive Lighthouse metrics visualization for React applications and any website. Built with React and Express, this tool offers an intuitive interface to analyze Core Web Vitals, performance metrics, and visual timelines of page loading.

### ✨ Key Features

- **📊 Comprehensive Performance Metrics**: Analyze First Contentful Paint (FCP), Largest Contentful Paint (LCP), Cumulative Layout Shift (CLS), and more
- **📱 Multi-Device Testing**: Switch between mobile and desktop strategies for accurate performance analysis
- **🎬 Visual Timeline**: Interactive filmstrips showing page loading progression
- **⚡ Real-time Analysis**: Get instant Lighthouse reports with detailed performance insights
- **🎯 Core Web Vitals Focus**: Specialized visualization for Google's Core Web Vitals metrics
- **🔧 Developer-Friendly**: Easy integration and deployment with modern web technologies

## 🛠️ Technology Stack

- **Frontend**: React 16.13.1, CSS3, Modern JavaScript (ES6+)
- **Backend**: Node.js, Express.js
- **Performance Testing**: Google Lighthouse 6.0.0, Puppeteer
- **Deployment**: Firebase Hosting, Glitch
- **Browser Automation**: Chrome Launcher, Puppeteer

## 📈 Performance Metrics Analyzed

### Core Web Vitals
- **Largest Contentful Paint (LCP)**: Measures loading performance
- **First Input Delay (FID)**: Measures interactivity
- **Cumulative Layout Shift (CLS)**: Measures visual stability

### Additional Performance Metrics
- **First Contentful Paint (FCP)**: Time to first content render
- **Speed Index**: How quickly content is visually displayed
- **Time to Interactive (TTI)**: When page becomes fully interactive
- **Total Blocking Time (TBT)**: Sum of all time periods between FCP and TTI
- **Server Response Time**: Backend performance measurement

## 🚀 Quick Start

### Prerequisites
- Node.js (v14 or higher)
- npm or yarn package manager
- Modern web browser

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/cra-metrics-visualizer.git
   cd cra-metrics-visualizer
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Start development server**
   ```bash
   # Start backend server
   npm run dev-server
   
   # In another terminal, start frontend
   npm run dev-client
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

### Production Deployment

```bash
# Build for production
npm run prod-build

# Start production server
npm start
```

## 📖 Usage Guide

### Basic Analysis
1. Enter any website URL in the input field
2. Choose between mobile or desktop strategy
3. Click "Analyze" to run Lighthouse performance audit
4. View comprehensive metrics and visual timeline

### Understanding Results
- **Green metrics**: Good performance scores
- **Orange metrics**: Needs improvement
- **Red metrics**: Poor performance requiring attention
- **Timeline visualization**: Shows loading progression with filmstrips

## 🔧 API Endpoints

### Lighthouse Analysis
```
GET /lighthouse?url={website_url}&strategy={mobile|desktop}
```

**Parameters:**
- `url` (required): Website URL to analyze
- `strategy` (optional): Testing strategy - 'mobile' or 'desktop' (default: mobile)

**Response:**
```json
{
  "audits": {
    "first-contentful-paint": { ... },
    "largest-contentful-paint": { ... },
    "cumulative-layout-shift": { ... }
  },
  "categories": { ... },
  "runtimeError": { ... }
}
```

### Health Check
```
GET /ping
```
Returns: `pong`

## 🏗️ Project Structure

```
cra-metrics-visualizer/
├── src/
│   ├── components/
│   │   ├── Header/           # Navigation and branding
│   │   ├── LighthouseAction/ # URL input and analysis trigger
│   │   ├── MetricsVisualizer/ # Main visualization component
│   │   │   ├── Timeline/     # Performance timeline
│   │   │   ├── Filmstrips/   # Loading progression
│   │   │   └── ClsMetric/    # Layout shift visualization
│   │   └── UI/              # Reusable UI components
│   ├── utils/
│   │   ├── constants/       # Application constants
│   │   ├── helpers/         # Utility functions
│   │   └── hooks/           # Custom React hooks
│   └── config.js           # Environment configuration
├── server.js               # Express backend server
└── package.json           # Dependencies and scripts
```

## 🎨 Customization

### Adding New Metrics
1. Update `src/utils/constants/index.js` with new metric definitions
2. Modify `src/App.js` to include the new metric in the analysis
3. Update visualization components as needed

### Styling
- CSS files are co-located with components
- Uses CSS custom properties for theming
- Responsive design with mobile-first approach

## 🚀 Deployment Options

### Firebase Hosting
```bash
npm run prod-build
firebase deploy
```

### Glitch
1. Import project to Glitch
2. Configure environment variables
3. Deploy automatically

### Docker (Custom)
```dockerfile
FROM node:14-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
RUN npm run prod-build
EXPOSE 5000
CMD ["npm", "start"]
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow React best practices
- Write meaningful commit messages
- Add tests for new features
- Ensure responsive design
- Optimize for performance

## 📄 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Google Lighthouse Team** for the powerful performance auditing tool
- **React Community** for excellent documentation and ecosystem
- **Web Performance Community** for Core Web Vitals standards
- **Open Source Contributors** who make projects like this possible

## 🔗 Live Demo

- **Production**: [https://cra-metrics-visualizer.firebaseapp.com](https://cra-metrics-visualizer.firebaseapp.com)
- **Development**: [https://anton-karlovskiy-cra-metrics-visualizer.glitch.me](https://anton-karlovskiy-cra-metrics-visualizer.glitch.me)

## 📞 Support

- **Issues**: [GitHub Issues](https://github.com/your-username/cra-metrics-visualizer/issues)
- **Discussions**: [GitHub Discussions](https://github.com/your-username/cra-metrics-visualizer/discussions)
- **Documentation**: [Wiki](https://github.com/your-username/cra-metrics-visualizer/wiki)

---

**Made with ❤️ for the web performance community**

*Optimize your web performance with comprehensive Lighthouse metrics visualization*