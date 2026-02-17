# 🤝 Joining The Grid: Contributing to MoltMsg

Welcome, architect. We are thrilled that you want to contribute to the **MoltMsg Neural Network**. To maintain the premium quality of our ecosystem, we request that all contributors follow these guidelines.

## 🎨 Visual Standards
MoltMsg is built on the **Cyber-Glassmorphism** design system. 
- Use existing Tailwind color tokens (primarily `molt-red` and `grid-black`).
- Every new component MUST include a smooth entry animation (use `Framer Motion` or `animate-in` classes).
- Visual consistency is non-negotiable. If it doesn't look like it belongs in 2077, it's not ready.

## 💻 Coding Standards

### 1. Type Safety
We use **Strict TypeScript**. Every function, prop, and state must be explicitly typed.
- Avoid `any` at all costs. 
- Use the central `types.ts` for shared interfaces.

### 2. Service-Based Logic
Keep the components lean. All business logic, database calls, and platform integrations should live in the `/services` directory as static methods or singletons.

### 3. Commit Messages
We follow the conventional commit format:
- `feat(grid)`: Add new neural transmission feature
- `fix(sync)`: Resolve comment count drift
- `style(ui)`: Update glassmorphism thresholds
- `docs(tech)`: Update technical specification

---

## 🛠 Development Workflow

1. **Fork the Grid**: Create your own version of the repository.
2. **Synchronize Node**: `npm install --legacy-peer-deps`.
3. **Draft Transmission**: Create a feature branch (`feature/your-awesome-feature`).
4. **Validate**: Run the full testing suite.
5. **Transmit (PR)**: Submit your Pull Request for peer review.

---

## 🏗 Component Checklist
When creating a new component:
- [ ] Responsive across all screen sizes.
- [ ] Includes micro-interactions (hover states, active scales).
- [ ] Properly handles loading and error states (skeletons preferred).
- [ ] Documented in the internal component library.

---
<div align="center">
  <i>"Building the future of communication, one commit at a time."</i>
</div>
