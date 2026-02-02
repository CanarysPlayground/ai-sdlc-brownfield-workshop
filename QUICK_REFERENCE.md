# Workshop Quick Reference Guide

## 🎯 At a Glance

This workshop covers **AI-Assisted Software Development** on a brownfield application.

---

## 📊 Workshop Overview

```
┌─────────────────────────────────────────────────────────────────┐
│                   AI-SDLC BROWNFIELD WORKSHOP                   │
│                                                                 │
│  Application: OctoCAT Supply Chain Management System           │
│  Feature: Cart Icon with Item Count Badge                     │
└─────────────────────────────────────────────────────────────────┘
```

---

## 🎓 Two Main Learning Paths

### 🛠️ Exercise 1: Development Persona (7.5-10 hours)
**Journey: Requirement → Code**

```
Phase 1 (2-3h)          Phase 2 (2.5-3h)         Phase 3 (3-4h)
──────────────          ───────────────          ──────────────
📝 Requirement          🏗️ Technical            🤖 Agentic
   Enrichment              Planning                Implementation

• Analyze app          • Design guardrails      • Implement CartContext
• Find gaps            • Spec Kit planning      • Build CartIcon
• Enrich specs         • Scaffold components    • Write tests
• Create Issue         • Execution plans        • Create PR
```

### 🧪 Exercise 2: Testing Persona (6.5-8 hours)
**Journey: Requirement → Test**

```
Phase 1 (2.5-3h)        Phase 2 (2.5-3h)         Phase 3 (1.5-2h)
───────────────         ───────────────          ──────────────
📋 Test Scenario       🔧 Test Automation       ✅ Test Execution
   Generation             Script Generation         & Reporting

• Analyze feature      • Setup Playwright       • Run test suite
• Generate scenarios   • Create test scripts    • Analyze results
• Create test plan     • Page object models     • Generate reports
• Coverage matrix      • Test utilities         • Bug tracking
```

---

## 🛠️ Key Technologies

| Category | Tools & Technologies |
|----------|---------------------|
| **AI Tools** | GitHub Copilot, Copilot Chat, Agent Mode, Spec Kit, Foundry Agent |
| **Frontend** | React, TypeScript, Vite, TailwindCSS, Context API |
| **Backend** | Node.js, Express |
| **Testing** | Vitest, React Testing Library, Playwright |
| **Tools** | Git, GitHub, VS Code, GitHub MCP |

---

## 📚 What You'll Learn

### Development Skills (Exercise 1)
- ✅ AI-assisted requirement enrichment
- ✅ Technical planning with AI
- ✅ Autonomous code generation
- ✅ React Context API & State Management
- ✅ Component architecture
- ✅ Accessibility (WCAG 2.1)
- ✅ Responsive design
- ✅ localStorage persistence
- ✅ Unit & integration testing

### Testing Skills (Exercise 2)
- ✅ AI-powered test scenario generation
- ✅ Test automation with Playwright
- ✅ Page object model pattern
- ✅ Cross-browser testing
- ✅ Accessibility testing
- ✅ Test reporting & metrics
- ✅ Bug tracking & quality assurance

---

## 🎯 Workshop Deliverables

### Exercise 1 Outputs:
```
├── docs/
│   ├── investigation/
│   │   └── cart-issue-analysis.md
│   ├── knowledge-repository/
│   │   ├── high-level-design.md
│   │   └── technical-design-document.md
│   └── specifications/
│       └── cart-icon-feature-requirements.md
├── .github/
│   └── instructions.md (design guardrails)
├── frontend/src/
│   ├── context/
│   │   ├── CartContext.tsx
│   │   └── CartContext.test.tsx
│   └── components/cart/
│       ├── CartIcon.tsx
│       └── CartIcon.test.tsx
└── Pull Request with implementation
```

### Exercise 2 Outputs:
```
├── tests/
│   ├── scenarios/
│   │   └── cart-test-plan.md
│   ├── e2e/
│   │   ├── cart-icon.spec.ts
│   │   └── cart-operations.spec.ts
│   └── reports/
│       └── test-execution-report.md
└── GitHub Issues for test stories
```

---

## ⚡ Quick Start Steps

1. **Read**: [WORKSHOP_SUMMARY.md](./WORKSHOP_SUMMARY.md) for full details
2. **Choose**: Development (Exercise 1) or Testing (Exercise 2) persona
3. **Start**: Follow phase-by-phase instructions
4. **Build**: Implement features with AI assistance
5. **Test**: Validate with comprehensive testing

---

## 🎓 Learning Outcomes Summary

After completing this workshop, you can:

**AI Skills**:
- ✅ Leverage AI for requirement analysis
- ✅ Guide AI agents effectively
- ✅ Review AI-generated code
- ✅ Use AI for test generation

**Engineering Skills**:
- ✅ Brownfield app development
- ✅ Full-stack feature implementation
- ✅ Test-driven development
- ✅ Modern React patterns
- ✅ Accessibility compliance

**Professional Skills**:
- ✅ Technical documentation
- ✅ Git workflows & PR reviews
- ✅ Quality assurance practices
- ✅ CI/CD integration

---

## 📖 Documentation Structure

```
ai-sdlc-brownfield-workshop/
├── README.md                    ← Start here
├── WORKSHOP_SUMMARY.md          ← Comprehensive overview
├── QUICK_REFERENCE.md           ← This file (at-a-glance)
└── Workshop-AI-SDLC/
    ├── Exercise 1/
    │   ├── 1. Enrich-requirement.md
    │   ├── 2. Technical Planning.md
    │   └── 3. Agentic Implementation.md
    └── Exercise 2/
        ├── 1. Test Scenario Generation.md
        ├── 2. Automation Script.md
        └── 3. Execute tests.md
```

---

## 🚀 Next Steps

1. **New here?** → Start with [README.md](./README.md)
2. **Want details?** → Read [WORKSHOP_SUMMARY.md](./WORKSHOP_SUMMARY.md)
3. **Ready to code?** → Begin [Exercise 1, Phase 1](./Workshop-AI-SDLC/Exercise%201/1.%20Enrich-requirement.md)
4. **Ready to test?** → Begin [Exercise 2, Phase 1](./Workshop-AI-SDLC/Exercise%202/1.%20Test%20Scenario%20Generation.md)

---

## ⏱️ Time Commitment

| Exercise | Total Time | Phases |
|----------|-----------|---------|
| Exercise 1: Development | 7.5-10 hours | 3 phases |
| Exercise 2: Testing | 6.5-8 hours | 3 phases |
| **Complete Workshop** | **14-18 hours** | **6 phases total** |

---

## 🎯 Prerequisites Checklist

- [ ] Visual Studio Code installed
- [ ] GitHub Copilot extension active
- [ ] GitHub account with Copilot access
- [ ] Node.js 18+ and npm
- [ ] Git installed and configured
- [ ] Basic JavaScript/TypeScript knowledge
- [ ] Understanding of React (for Exercise 1)
- [ ] Testing concepts familiarity (for Exercise 2)

---

## 💡 Pro Tips

- **Pace yourself**: Each phase builds on the previous
- **Use AI actively**: Don't just read, interact with Copilot
- **Test frequently**: Validate changes incrementally
- **Document as you go**: Notes help with learning
- **Ask questions**: Use Copilot Chat when stuck

---

**Ready to start your AI-assisted development journey?** 🚀

Choose your path:
- 👨‍💻 [Development Persona (Exercise 1)](./Workshop-AI-SDLC/Exercise%201/1.%20Enrich-requirement.md)
- 🧪 [Testing Persona (Exercise 2)](./Workshop-AI-SDLC/Exercise%202/1.%20Test%20Scenario%20Generation.md)
