# 🎓 EduPulse

**Real-time, Anonymous Classroom Feedback System**

EduPulse helps educators understand student confusion as it happens—without forcing students to speak up. A silent signal for better equity in education.

[![Next.js](https://img.shields.io/badge/Next.js-16.1.1-black)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)](https://www.typescriptlang.org/)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL-green)](https://supabase.com/)

---

## 📋 Table of Contents

- [About](#about)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Demo Credentials](#demo-credentials)
- [Project Structure](#project-structure)
- [Environment Setup](#environment-setup)
- [Usage Guide](#usage-guide)
- [SDG-4 Alignment](#sdg-4-alignment)
- [Contributing](#contributing)

---

## 🎯 About

EduPulse addresses the **"Silent Classroom" problem** where 80% of confused students never ask questions due to:
- Fear of judgment
- Language barriers
- Fast-paced lectures
- Social anxiety

Our solution provides a **one-click, anonymous feedback mechanism** that gives educators real-time insights into classroom understanding.

---

## ✨ Features

### For Students
- ✅ **Anonymous Signaling** - No login required, complete privacy
- 📍 **Geofenced Access** - Signals only work within campus boundaries
- ⚡ **One-Click Feedback** - "I'm Confused" button with optional context
- 🔒 **Secure & Private** - No tracking, no data collection on individuals

### For Educators
- 📊 **Live Dashboard** - Real-time confusion metrics and trends
- 🤖 **AI Insights** - Smart suggestions based on signal patterns
- 📈 **Historical Trends** - Visualize confusion over time (last hour)
- 🎯 **Actionable Data** - See location clusters and signal types

### For Admins
- 🗺️ **Campus Geofencing** - Configure campus boundaries (lat/lng/radius)
- 🎛️ **Signal Management** - Add/remove custom signal types
- 📊 **System Overview** - Monitor active sessions and usage stats
- 🔄 **Data Reset** - Password-protected demo data management

---

## 🛠️ Tech Stack

- **Frontend**: Next.js 16.1.1 (App Router), React, TypeScript
- **Styling**: Tailwind CSS (Vanilla CSS approach)
- **Backend**: Supabase (PostgreSQL)
- **Icons**: Lucide React
- **Fonts**: Inter (Google Fonts)
- **Geolocation**: Browser Geolocation API + Haversine formula

---

## 🔑 Demo Credentials

### Admin Dashboard Access

**URL**: `http://localhost:3000/admin`

**Demo Admin Password**: `edupulse2026`

> **Note**: For production, change the admin password and use proper bcrypt hashing. The current setup is for demonstration purposes only.

### Test Locations

To test geofencing, you'll need to:
1. Update `campus_settings` table with your actual campus coordinates
2. Use browser developer tools to mock your location (if testing remotely)
3. Or physically be within the configured radius

**Mock Location in Chrome DevTools**:
1. Open DevTools (F12)
2. Press `Ctrl+Shift+P` → Type "Sensors"
3. Select "Sensors" tab
4. Choose "Other" and enter your campus lat/lng

---

## 📁 Project Structure

```
edu-pulse/
├── app/
│   ├── actions/          # Server actions
│   │   ├── admin.ts      # Admin operations
│   │   └── signals.ts    # Signal operations
│   ├── admin/            # Admin dashboard
│   │   └── page.tsx
│   ├── educator/         # Educator views
│   │   └── dashboard/
│   │       └── page.tsx
│   ├── student/          # Student view
│   │   └── page.tsx
│   ├── impact/           # SDG-4 impact page
│   │   └── page.tsx
│   ├── layout.tsx        # Root layout
│   ├── page.tsx          # Landing page
│   └── globals.css       # Global styles
├── utils/
│   └── supabase/         # Supabase client setup
│       ├── client.ts
│       └── server.ts
├── middleware.ts         # Route protection
├── .env.local            # Environment variables (create this)
└── README.md
```

---

## 🎮 Usage Guide

### Student Flow

1. Navigate to `/student`
2. Allow browser location access
3. Verify you're within campus boundaries
4. Click "I'm Confused" when lost
5. Optionally add room number and brief context
6. Signal sent anonymously to educator dashboard

### Educator Flow

1. Navigate to `/educator/dashboard`
2. View live confusion pulse chart
3. Monitor current confusion percentage
4. Read AI-generated insights
5. Check recent activity feed
6. Adjust teaching based on real-time feedback

### Admin Flow

1. Navigate to `/admin`
2. Enter admin password: `edupulse2026`
3. Configure campus geofence coordinates
4. Add/remove custom signal types
5. Monitor system-wide statistics
6. Reset demo data when needed

---

## 🌍 SDG-4 Alignment

**Sustainable Development Goal 4**: Quality Education

### How EduPulse Contributes:

**Equity** 🤝
- Removes barriers for shy, non-native speakers, or anxious students
- Ensures all voices are heard without fear of judgment

**Inclusion** 🌈
- Anonymous system protects vulnerable students
- No login requirement reduces technical barriers

**Quality** 📚
- Real-time feedback enables immediate teaching adjustments
- Data-driven insights help educators identify systemic issues

**Access** 🌐
- Browser-based, no app download required
- Works on any device with internet connection

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Development Guidelines

- Follow TypeScript best practices
- Use Tailwind CSS for styling
- Write meaningful commit messages
- Test geofencing functionality before submitting
- Ensure mobile responsiveness

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- Built for **EDVentures 2026 Competition**
- Inspired by the need for equitable classroom feedback
- Designed to support **SDG-4: Quality Education**

---

## 📞 Contact

**Project Maintainer**: Kuldeep Mishra

For questions, feedback, or collaboration opportunities, please open an issue on GitHub.

---

<div align="center">
  <strong>EduPulse</strong> • Making education more equitable, one signal at a time 🎓
</div>
