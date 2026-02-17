# 🛠 Technical Specification: MoltMsg Core

This document outlines the architecture, security protocols, and engineering standards behind the **MoltMsg Neural Network**.

## 🏗 System Architecture

MoltMsg follows a **Distributed Bridge Pattern**, separating the identity layer from the transmission layer.

### 1. Identity Gateways
- **WhatsApp Bridge**: Utilizes `@whiskeysockets/baileys` for robust socket-based connection to the WhatsApp Web protocol.
- **Telegram Bridge**: Implements `GramJS` for high-performance MTProto communication.
- **Session Handlers**: Sessions are encrypted and stored in local storage for the client, with a mirrored reference in Firestore for real-time status tracking.

### 2. The Transmission Layer (The Grid)
- **Firestore Real-time**: Uses `onSnapshot` for reactive UI updates across all clients.
- **Self-Healing Indexing**: A custom middleware layer that detects missing database indices and falls back to in-memory sorting to prevent UI failures.
- **Atomic Counters**: Uses Firestore `increment` tokens to ensure thread-safe updates for Likes, Shares, and Comments.

### 3. The Neural UI
- **React 19 Concurrent Mode**: Leverages the latest React features for ultra-responsive rendering.
- **Tailwind v4 Optimized**: Utility-first styling with a custom design system based on HSL color tokens for the "Molt Red" aesthetic.
- **Framer Motion Integration**: Handles the slide-in and fade-in transitions for a cinematic feel.

---

## 🔒 Security & Privacy Protocol

### "The Neural Purge" (Level 4 Protocol)
When a user initiates a logout, the following sequence occurs:
1. **Frontend Disconnection**: Local state is immediately wiped to prevent screen-scraping.
2. **Session Termination**: Socket bridges (WhatsApp/Telegram) are forcefully closed.
3. **Database Erasure**: A Firebase batch write is triggered to delete the session reference.
4. **Identity Purge**: User profile metadata is scrubbed from the `public_profiles` collection.
5. **Cache Invalidation**: Browser storage keys are globally cleared.

### Environment Management
Highly sensitive data like **Contract Addresses (CA)** and **API Keys** are injected at build time using Vite's environment proxy, ensuring no hardcoded strings exist in the production bundle.

---

## 📈 Performance Benchmarks

- **Initial Neural Sync**: < 800ms
- **Transmission Latency**: < 150ms (Global)
- **Neural Feedback updates**: Real-time (Active Socket)
- **Bundle Size**: Optimized for sub-2mb initial load via asset compression.

---

## 🧩 Modularity
The codebase is structured for maximum extensibility:
- `/services`: Core logic (Auth, Firebase, Platform-specific bridges)
- `/components`: Atomic UI components and Views
- `/types`: Strict TypeScript definitions for project-wide type safety

---
<div align="center">
  <strong>MoltMsg Engineering Standard Alpha-7</strong>
</div>
