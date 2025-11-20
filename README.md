# MioCity Network

<div align="center">
  <h3>🌐 React Native BuddyBoss Community App + macOS Business Manager</h3>
  <p>A complete mobile application that replicates the full BuddyBoss experience</p>
  <p><strong>NEW:</strong> macOS Desktop Business Management Control Center</p>
</div>

---

## 🖥️ macOS Business Manager (NEW!)

A native macOS desktop application for business owners and managers to efficiently manage their operations.

**Features:**

- 📦 Unified Order Management (all order types)
- 🛍️ Product Management with bulk import/export
- 📋 Visual Menu Editor
- 📊 Analytics & Reporting Dashboard
- 🔔 Desktop Notifications
- 🎯 System Tray Integration

**Quick Start:**

```bash
cd desktop
./install.sh
npm run dev
```

**Documentation:** See [`desktop/README.md`](./desktop/README.md) for full details.

---

## 🚀 Quick Start (After Setup Issues)

If you're continuing after troubleshooting, see:

- **Quick Reference:** [`QUICK_START_AFTER_RESTART.md`](./QUICK_START_AFTER_RESTART.md)
- **Full Documentation:** [`TROUBLESHOOTING_SESSION.md`](./TROUBLESHOOTING_SESSION.md)

**TL;DR:** Ensure Full Disk Access for Xcode/Terminal in System Settings, restart both, then build with `⌘ + R`.

---

## 📱 About

**MioCity Network** is a React Native mobile application designed to connect with WordPress + BuddyBoss backends, providing a full-featured social networking experience. The app mirrors the official BuddyBoss app functionality and integrates seamlessly with the BuddyBoss REST API and App API.

### ✨ Key Features

- 🔐 **Authentication** - JWT/OAuth2 login, registration, and password recovery
- 📰 **Activity Feed** - View, create, like, and comment on activities
- 👥 **Groups** - Browse, join, and manage community groups
- 💬 **Messaging** - Private messaging and conversations
- 🔔 **Notifications** - Real-time push notifications via Firebase
- 👤 **User Profiles** - View and edit member profiles
- 🎥 **Video Platform** - Multi-platform video integration (YouTube, Facebook, Instagram)
- ⚙️ **Settings** - Customize notifications, privacy, and preferences
- 🌍 **Multi-language Support** - Language selection
- 🎨 **Theme Support** - Light/Dark/Auto themes
- 📴 **Offline Mode** - Cache data for offline access

#### 🎥 Video Platform Features (NEW!)

- ✅ **YouTube Integration** - OAuth connection, video import, trending feed
- ✅ **Facebook Integration** - OAuth connection, video import, Facebook Reels
- ✅ **Instagram Integration** - OAuth connection, Reels import
- 🎬 **Smart Video Feed** - Mixed user content + global trending videos
- 📱 **YouTube-inspired UI** - Modern video feed with shorts and long videos
- ⚡ **Smart Import Queue** - Automatic video import with server load management
- 🔒 **Platform Compliance** - Full YouTube API Terms compliance

**See:** [server-files/Video/FACEBOOK_INSTAGRAM_SETUP.md](server-files/Video/FACEBOOK_INSTAGRAM_SETUP.md) for setup instructions.

---

## 🛠️ Tech Stack

| Category               | Technology                             |
| ---------------------- | -------------------------------------- |
| **Framework**          | React Native 0.73+ with TypeScript     |
| **State Management**   | Zustand                                |
| **Navigation**         | React Navigation (Stack + Bottom Tabs) |
| **API Client**         | Axios with interceptors                |
| **Storage**            | MMKV (fast key-value storage)          |
| **Push Notifications** | Firebase Cloud Messaging (FCM)         |
| **Authentication**     | JWT tokens with refresh                |
| **Backend**            | WordPress + BuddyBoss Platform         |

---

## 📂 Project Structure

```
MiocityAppReact/
├── src/
│   ├── api/                  # API client and endpoints
│   │   ├── client.ts         # Axios instance with interceptors
│   │   └── endpoints.ts      # BuddyBoss API endpoints
│   ├── components/           # Reusable UI components
│   ├── constants/            # Colors, spacing, theme constants
│   ├── hooks/                # Custom React hooks
│   ├── navigation/           # Navigation configuration
│   │   ├── RootNavigator.tsx
│   │   ├── AuthNavigator.tsx
│   │   └── MainNavigator.tsx
│   ├── screens/              # Screen components
│   │   ├── auth/             # Login, Register, etc.
│   │   ├── feed/             # Activity feed screens
│   │   ├── groups/           # Groups screens
│   │   ├── messages/         # Messaging screens
│   │   ├── notifications/    # Notifications screen
│   │   └── profile/          # Profile screens
│   ├── services/             # App services (Firebase, etc.)
│   ├── store/                # Zustand state management
│   │   ├── authStore.ts
│   │   └── activityStore.ts
│   ├── types/                # TypeScript type definitions
│   │   ├── api.types.ts
│   │   └── navigation.types.ts
│   └── utils/                # Utility functions
│       └── storage.ts        # MMKV storage helpers
├── android/                  # Android native code
├── ios/                      # iOS native code
├── App.tsx                   # Root component
├── package.json
└── tsconfig.json
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** >= 18.0.0
- **npm** >= 9.0.0
- **React Native CLI**
- **Xcode** (for iOS development)
- **Android Studio** (for Android development)

### Installation

1. **Clone the repository**

   ```bash
   cd MiocityAppReact
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Install iOS dependencies** (macOS only)

   ```bash
   cd ios && pod install && cd ..

   ```

4. **Configure environment variables**

   ```bash

   cp .env.example .env
   ```

   Edit `.env` with your BuddyBoss server details:

   ```
   API_BASE_URL=https://your-buddyboss-site.com
   APP_ID=your_app_id
   APP_SECRET=your_app_secret

   ```

5. **Run the app**

   **iOS:**

   ```bash
   npm run ios
   ```

   **Android:**

   ```bash
   npm run android
   ```

---

## 📚 BuddyBoss API Integration

This app integrates with the official BuddyBoss REST API and App API:

- **Base URL**: `https://your-site.com/wp-json/`
- **Auth Endpoint**: `/buddyboss-app/v1/auth/login`
- **Activity Endpoint**: `/buddyboss/v1/activity`
- **Groups Endpoint**: `/buddyboss/v1/groups`
- **Messages Endpoint**: `/buddyboss/v1/messages`
- **Members Endpoint**: `/buddyboss/v1/members`

### 📖 Documentation Resources

- [BuddyBoss App Development Docs](https://www.buddyboss.com/resources/dev-docs/app-development/extending-the-buddyboss-app-plugin/)
- [BuddyBoss REST API Reference](https://www.buddyboss.com/resources/api/app/)
- [BuddyBoss Support Forums](https://www.buddyboss.com/support/)

---

## 🔧 Development Scripts

| Command              | Description                       |
| -------------------- | --------------------------------- |
| `npm start`          | Start Metro bundler               |
| `npm run ios`        | Run on iOS simulator              |
| `npm run android`    | Run on Android emulator           |
| `npm test`           | Run Jest tests                    |
| `npm run lint`       | Run ESLint                        |
| `npm run lint:fix`   | Fix ESLint issues                 |
| `npm run type-check` | Run TypeScript compiler check     |
| `npm run format`     | Format code with Prettier         |
| `npm run clean`      | Clean build artifacts             |
| `npm run backup`     | Create Git backup and zip archive |

---

## 🏗️ Build for Production

### Android

```bash
npm run build:android
# Output: android/app/build/outputs/apk/release/app-release.apk
```

### iOS

```bash
npm run build:ios
# Or use Xcode for App Store builds
```

---

## 🧪 Testing

```bash
# Run all tests
npm test

# Run tests in watch mode
npm test -- --watch

# Generate coverage report
npm test -- --coverage
```

---

## 🔐 Environment Configuration

The app uses `react-native-config` for environment variables. Create a `.env` file based on `.env.example`:

```env
# API Configuration
API_BASE_URL=https://your-buddyboss-site.com
APP_ID=your_app_id
APP_SECRET=your_app_secret
API_TIMEOUT=30000

# Firebase
FCM_SERVER_KEY=your_fcm_server_key
FCM_SENDER_ID=your_fcm_sender_id

# Feature Flags
ENABLE_OFFLINE_MODE=true
ENABLE_PUSH_NOTIFICATIONS=true
DEBUG_API_CALLS=true

```

---

## 📱 Features Roadmap

### ✅ Completed

- [x] Project structure and configuration

- [x] Authentication flow (Login/Register)
- [x] Navigation setup (Stack + Bottom Tabs)
- [x] API client with interceptors
- [x] Activity feed display
- [x] Zustand state management
- [x] Firebase push notifications setup

### 🚧 In Progress

- [ ] Complete registration screen
- [ ] Profile editing
- [ ] Groups functionality
- [ ] Messaging system
- [ ] Notifications screen

### 📋 Planned

- [ ] Media uploads (images/videos)
- [ ] Friend system
- [ ] Search functionality
- [ ] Advanced filters
- [ ] Offline data caching
- [ ] Analytics integration
- [ ] Biometric authentication
- [ ] App localization (i18n)

---

## � MCP Server (Development Assistant)

This project includes a **Model Context Protocol (MCP) Server** that provides intelligent development assistance.

### Features

- 📋 **Roadmap Tracking** - Always know the current phase and progress
- 📝 **Task Management** - Get next tasks automatically
- 🔍 **Documentation Search** - Quick access to all project docs
- 🌐 **API Reference** - Instant BuddyBoss API endpoint lookup
- 📊 **Progress Monitoring** - Track development status

### Setup

```bash
# Install MCP server dependencies
cd mcp-server
npm install
npm run build
```

### Usage with Claude Desktop

Add to `~/Library/Application Support/Claude/claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "miocity-network": {
      "command": "node",
      "args": ["/path/to/MiocityAppReact/mcp-server/dist/index.js"]
    }
  }
}
```

### Usage with Cline (VS Code)

Already configured in `.vscode/cline_mcp_settings.json`

### Example Queries

- "What's the current development phase?"
- "Show me the next 5 tasks"
- "Search for authentication in the docs"
- "What API endpoints are available for groups?"

See `mcp-server/README.md` for detailed documentation.

---

## �🤝 Contributing

This is a private project for MioConnex platform. If you're part of the team:

1. Create a feature branch (`git checkout -b feature/amazing-feature`)
2. Commit your changes (`git commit -m 'Add amazing feature'`)
3. Push to the branch (`git push origin feature/amazing-feature`)
4. Open a Pull Request

---

<support@mioconnex.com>

## 📄 License

Proprietary - MioConnex Platform &copy; 2024

---

## 🆘 Support & Contact

For questions or support:

- **Email**: <support@mioconnex.com>
- **Documentation**: [Internal Wiki]
- **Issue Tracker**: GitHub Issues

---

## 🙏 Acknowledgments

- [BuddyBoss](https://www.buddyboss.com/) for the excellent platform and API
- React Native community
- All contributors to the open-source libraries used in this project

---

<div align="center">
  <p>Built with ❤️ for the MioConnex Platform</p>
</div>
