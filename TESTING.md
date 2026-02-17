# 🧪 Testing Protocol: MoltMsg

To maintain the high-fidelity integrity of the **MoltMsg Neural Network**, we follow a rigorous testing strategy. Every transmission and synchronization node must be validated.

## 🛠 Testing Tools
- **Vite Test Runner**: Optimized for lightning-fast unit tests.
- **Firebase Emulator Suite**: Used for local validation of Firestore rules and Atomic Counters.
- **Neural Mocking**: Custom mock providers for WhatsApp (`Baileys`) and Telegram (`GramJS`) identities.

---

## 🏃 Running Tests

### 1. Unit Tests
Validate core services and utility functions.
```bash
npm test
```

### 2. Integration Tests (Neural Sync)
Test the real-time synchronization between the local client and the Firebase Cloud Node.
```bash
# Requires Firebase Emulator
npm run test:integration
```

### 3. Component Snapshots
Ensure the Cyber-Glassmorphism UI remains consistent across all viewports.
```bash
npm run test:ui
```

---

## 📋 Test Coverage Areas

### 🧬 Identity Sync
- Successfully connecting via WhatsApp QR code.
- Telegram OTP verification flow.
- Auto-restoration of sessions after a disconnect.

### 📡 The Grid (Feed)
- Real-time `onSnapshot` delivery of new transmissions.
- Multi-client synchronization of Like and Share counts.
- Fallback logic when database indices are not yet propagated.

### 🧹 The Neural Purge
- **Verification**: Ensure no `auth_keys` or `session_ids` remain in local storage after logout.
- **Database Cleanup**: confirm that `public_profiles` and active `sessions` are physically removed from the cloud node.

---

## 🧪 Manual QA Checklist
Before pushing any transmission code to the main branch, verify:
- [ ] UI scales perfectly on mobile devices (Responsive Grid).
- [ ] Comment count updates instantly in the main feed.
- [ ] Contract Address (CA) is correctly loaded from environment variables.
- [ ] No hardcoded Firebase credentials in the logic layer.

---
<div align="center">
  <strong>Excellence is not an act, but a synchronization.</strong>
</div>
