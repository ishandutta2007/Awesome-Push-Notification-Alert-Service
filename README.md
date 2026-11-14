# Awesome-Push-Notification-Alert-Service

# Awesome Push Notification & Alert Service

> A curated list of top Push Notification and Alert Service platforms — both SaaS/Hosted commercial messaging solutions and open-source alternatives for delivering real-time alerts across push, email, SMS, and in-app channels.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [OneSignal](#onesignal)
  - [Firebase Cloud Messaging](#firebase-cloud-messaging)
  - [Airship](#airship)
  - [Braze](#braze)
  - [Courier](#courier)
  - [MagicBell](#magicbell)
  - [WonderPush](#wonderpush)
  - [Pusher](#pusher)
  - [Zoho Catalyst Push Notifications](#zoho-catalyst-push-notifications)
- [Open-Source Software](#-open-source-software)
  - [Novu](#novu)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Push Notification and Alert Service platforms. These are not open-source but are included as reference points for feature comparison.

### OneSignal
**Type:** Multi-channel engagement with generous free tier
OneSignal provides push notifications, email, SMS, and in-app messaging from a single platform, with SDKs for every major language and framework . The free plan supports up to 10,000 subscribers with unlimited notifications, making it the most accessible entry point for small teams . It offers segmentation by session count, tags, language, and country, plus scheduling, A/B testing, and delivery analytics . API rate limits are 150 requests/second on free plans and 6,000 on paid plans .  
**Best for:** Teams wanting a proven, multi-channel notification platform with a genuinely usable free tier and broad SDK support.

### Firebase Cloud Messaging
**Type:** Google-native push infrastructure for mobile and web
Firebase Cloud Messaging (FCM) is Google's free push notification service, deeply integrated with Android and available for iOS and web via service workers . It handles token management, topic messaging, and platform-specific delivery (APNs for iOS, Web Push for browsers). The server-side Admin SDK supports Node.js, Java, Python, and Go, with straightforward message payloads for notifications and data . **Trade-off:** It is infrastructure rather than a full engagement platform—you build segmentation, scheduling, and analytics yourself.  
**Best for:** Teams already in the Google/Firebase ecosystem wanting reliable, free push delivery at scale without per-message costs.

### Airship
**Type:** Mobile-first customer experience platform
Airship provides push notifications, in-app messages, Message Center (app inbox), email, SMS, and open channel messaging with AI-powered orchestration . It supports deep segmentation, journey mapping, and real-time analytics. Gartner reviewers note it is a "set and forget" system after initial configuration .  
**Best for:** Enterprises wanting a comprehensive mobile engagement platform with strong orchestration and multi-channel capabilities beyond simple push.

### Braze
**Type:** Enterprise customer engagement with journey orchestration
Braze provides cross-channel messaging, journey orchestration (Canvas), AI-powered experimentation, and a SQL Query Builder . Reviewers praise its reliable data connectivity, intuitive interface for non-technical users, and strong Customer Success team, though some note uneven development focus (newer AI/WhatsApp features get more attention than core click/open accuracy) .  
**Best for:** Large enterprises with dedicated marketing operations teams needing sophisticated multi-channel journeys and real-time data activation.

### Courier
**Type:** Notification API with unified multi-channel delivery
Courier provides a notification API that routes messages across email, push, SMS, and chat with a single API call. Pricing is based on notifications sent: Developer is free for 10,000 sends/month, Business is pay-as-you-go at $0.005 per send, and Enterprise is custom .  
**Best for:** Developers wanting a unified API to abstract away channel-specific delivery logic without building each integration individually.

### MagicBell
**Type:** Notification infrastructure with in-app inbox
MagicBell focuses on product notification infrastructure, including an embeddable in-app notification inbox alongside push, email, SMS, and Slack delivery. Pricing is delivery-based: Builder is free for 1,000 deliveries/month, Startup is $249/month for 50,000 deliveries with overages at $0.0025, and Enterprise is custom . **Important:** Deliveries are counted per channel, so multi-channel notifications consume quota faster .  
**Best for:** Product teams wanting a ready-made notification inbox component alongside multi-channel delivery, accepting that pricing scales with channel fan-out.

### WonderPush
**Type:** Subscriber-based pricing with all features included
WonderPush charges €1 per 1,000 subscribers per month, with all features (rich formats, automation, segmentation, analytics) included at every tier . A 14-day free trial is available without a credit card. Subscribers are counted as unique device + app/website combinations, and unsubscribed devices are excluded from billing .  
**Best for:** Teams wanting predictable, subscriber-based pricing with no feature gating, particularly those with high notification volume per subscriber.

### Pusher
**Type:** Real-time messaging infrastructure
Pusher provides real-time channels for live notifications, chat, and collaboration, with pricing starting at $699/month for Growth (40M messages, 15K connections) . It is positioned for real-time bidirectional communication rather than one-way push alerts, with SLAs available for enterprise customers .  
**Best for:** Applications needing real-time bidirectional messaging (chat, live updates) rather than traditional one-way push notifications.

### Zoho Catalyst Push Notifications
**Type:** Push notifications within Zoho Catalyst serverless platform
Zoho Catalyst provides push notification capabilities as part of its serverless platform, allowing developers to send notifications to web app users (up to 50 users per function call) by user ID or email address . It is tightly integrated with Catalyst's authentication and user management, making it the natural choice for teams already building on Zoho's serverless stack .  
**Best for:** Teams already using Zoho Catalyst for their application backend wanting integrated push notifications without a separate vendor.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Push Notification and Alert Service tools. The open-source ecosystem is **anchored by Novu** as the leading notification infrastructure platform.

### Novu
**Stack:** TypeScript / NestJS / MongoDB / Redis | **License:** MIT
Novu is the leading open-source notification infrastructure platform, providing a unified API and visual dashboard for managing multi-channel notifications without per-message pricing . Key features include:
- **Multi-channel delivery**: email, SMS, push, in-app inbox, Slack, Teams, Discord, WhatsApp 
- **Visual workflow editor**: drag-and-drop flow builder with conditions, delays, and digest 
- **Embeddable in-app notification center**: React, Angular, and Vue components 
- **Subscriber preference management**: users control which channels they receive notifications on 
- **Content management**: template editor with variable interpolation and i18n support 
- **Delivery observability**: track notification status, delivery rates, and failures 

The architecture consists of an API server, a Worker service processing the notification queue asynchronously, a WebSocket server for real-time in-app delivery, and a Dashboard SPA for visual management . Deploys via Docker Compose or Railway with MongoDB and Redis . **Trade-off:** Self-hosting means you own the infrastructure, and some enterprise features may be gated to the managed cloud offering.  
**Best for:** Teams wanting full control over their notification infrastructure with a unified API and visual workflow builder, avoiding per-message pricing and vendor lock-in.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Free Tier | Multi-Channel | Self-Hosted | Best For |
|----------|---------|-------|-----------|---------------|-------------|----------|
| **OneSignal** | Proprietary | Cloud | ✅ 10K subscribers | ✅ Push/Email/SMS/In-App | ❌ | Free multi-channel start |
| **Firebase FCM** | Proprietary | Cloud | ✅ Free | (Push only) | ❌ | Google-native push |
| **Airship** | Proprietary | Cloud | Trial | ✅ Push/Email/SMS/In-App | ❌ | Enterprise mobile engagement |
| **Braze** | Proprietary | Cloud | Trial | ✅ Full journey orchestration | ❌ | Enterprise marketing ops |
| **Courier** | Proprietary | Cloud | ✅ 10K sends | ✅ Email/Push/SMS/Chat | ❌ | Unified notification API |
| **MagicBell** | Proprietary | Cloud | ✅ 1K deliveries | ✅ Push/Email/SMS/Slack | ❌ | Product notification inbox |
| **WonderPush** | Proprietary | Cloud | Trial (14d) | ✅ Push only | ❌ | Subscriber-based pricing |
| **Novu** | MIT | TypeScript/MongoDB | ✅ Self-host | ✅ Full multi-channel | ✅ | Full OSS notification infra |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Push Notification or Alert Service tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem for **full notification infrastructure** is led by **Novu**, which provides a unified API, visual workflow builder, and multi-channel delivery under MIT licensing . For teams wanting a free starting point with minimal setup, **OneSignal** and **Firebase FCM** are the most accessible commercial options, though neither is open-source. Commercial platforms like Airship and Braze remain far more capable for enterprise-scale journey orchestration and analytics, but at significantly higher cost and complexity.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
