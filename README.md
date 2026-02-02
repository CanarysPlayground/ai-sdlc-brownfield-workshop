# AI-SDLC Brownfield Workshop

Welcome to the **AI-SDLC Brownfield Workshop**! This comprehensive hands-on workshop teaches you how to leverage GitHub Copilot and AI agents throughout the entire software development lifecycle on a brownfield application - the **OctoCAT Supply Chain Management System**.

## 🌟 Key Highlights

**What Makes This Workshop Unique:**
- ✨ **AI-First Approach**: Learn to use GitHub Copilot, Agent Mode, Spec Kit, and Foundry Agent for autonomous development
- 🏗️ **Brownfield Focus**: Work on existing codebase, identify gaps, and implement missing features (Cart Icon with badge)
- 🔄 **Complete SDLC Coverage**: From requirement enrichment → technical planning → implementation → testing → CI/CD
- 👥 **Dual Personas**: Experience both Development and Testing perspectives
- 🎯 **Practical Outcomes**: Build production-ready features with 80%+ test coverage and full accessibility compliance

**Real-World Skills You'll Master:**
- AI-assisted requirement enrichment and GitHub Issue creation
- Technical planning with design guardrails and component scaffolding  
- Autonomous code generation with Copilot Agent Mode
- BDD test automation with Selenium and Behave framework
- CI/CD integration with Azure Playwright Testing
- Full-stack implementation (React Context API, localStorage, toast notifications)
- WCAG 2.1 accessibility compliance and responsive design

## 🎯 Quick Start

**New to this workshop?** Choose your documentation style:

- 📖 **[WORKSHOP_SUMMARY.md](./WORKSHOP_SUMMARY.md)** - Comprehensive detailed overview (recommended for first read)
- ⚡ **[QUICK_REFERENCE.md](./QUICK_REFERENCE.md)** - Visual at-a-glance guide (quick lookup)
- 📚 **This README** - Navigation hub and getting started

## 📚 Workshop Exercises

### 🛠️ Exercise 1: Development Persona (Requirement to Code)
**Goal**: Implement a complete cart icon feature from requirement enrichment to production-ready code  
**Time**: ~10-12 hours total (for feature implementation, not workshop phases)

- **Phase 1**: [Knowledge Ingestion & Requirement Enrichment](./Workshop-AI-SDLC/Exercise%201/1.%20Enrich-requirement.md)
  - Analyze brownfield app with Copilot Chat
  - Build knowledge repository from existing docs
  - Identify missing requirements (cart icon gap)
  - Create comprehensive GitHub Issue with MCP
  
- **Phase 2**: [Technical Planning & Scaffolding](./Workshop-AI-SDLC/Exercise%201/2.%20Technical%20Planning.md)
  - Use Spec Kit to break down issue into technical tasks
  - Create design guardrails (`.github/instructions.md`)
  - Scaffold CartContext and CartIcon components
  - Generate execution plans and milestones
  
- **Phase 3**: [Agentic Implementation](./Workshop-AI-SDLC/Exercise%201/3.%20Agentic%20Implementation.md) (3-4 hours)
  - Implement CartContext with localStorage persistence
  - Build CartIcon component with dynamic badge
  - Integrate toast notifications (react-hot-toast)
  - Write comprehensive tests (>80% coverage)
  - Create PR with AI-generated summaries

### 🧪 Exercise 2: Testing Persona (Requirement to Test)
**Goal**: Generate comprehensive test scenarios and automate testing for the cart feature  
**Time**: ~9.5-11.5 hours total

- **Phase 1**: [Test Scenario Generation](./Workshop-AI-SDLC/Exercise%202/1.%20Test%20Scenario%20Generation.md) (2.5-3 hours)
  - Use Foundry Agent to analyze requirements
  - Generate 100+ test scenarios covering functional, non-functional, and edge cases
  - Create test coverage matrix
  - Document test plans in GitHub Issues
  
- **Phase 2**: [Automation Scripting with BDD](./Workshop-AI-SDLC/Exercise%202/2.%20Autoamtion%20Script.md) (3.5-4 hours)
  - Use Copilot Custom Agent to generate Selenium scripts (Python)
  - Implement BDD with Behave framework (Cucumber for Python)
  - Create Gherkin feature files and step definitions
  - Implement Page Object Model (POM) pattern
  - Configure multi-browser testing (Chrome, Firefox, Edge)
  
- **Phase 3**: [CI/CD Integration with Azure Playwright](./Workshop-AI-SDLC/Exercise%202/3.%20Execute%20tests.md) (3.5-4.5 hours)
  - Push automation code to GitHub
  - Create GitHub Actions workflows for CI/CD
  - Configure Azure Playwright Testing workspace
  - Execute tests in Azure cloud environment
  - Generate reports and setup notifications (Slack, Teams)
  - Implement scheduled test runs and dashboards

## 🚀 What You'll Build

**Feature**: Cart Icon with Item Count Badge for OctoCAT Supply Chain System

**Deliverables:**
- 🛒 Cart icon component with dynamic badge showing item count
- 💾 localStorage persistence for cart state across page refreshes
- 🔔 Toast notifications for user feedback (using react-hot-toast)
- 📄 Cart page with full CRUD operations (add, remove, update, clear)
- 🧪 Comprehensive test suite with 80%+ code coverage
- ♿ WCAG 2.1 Level AA accessibility compliance
- 📱 Fully responsive design (mobile, tablet, desktop)
- 🌙 Dark mode support
- 🤖 100+ automated test scenarios using BDD approach
- ☁️ CI/CD pipeline with Azure cloud execution

## 🛠️ Technologies & Tools Stack

### Frontend Development
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite
- **Styling**: TailwindCSS with dark mode
- **State Management**: React Context API
- **Icons**: Heroicons
- **Notifications**: react-hot-toast
- **Persistence**: localStorage API

### Backend Development
- **Runtime**: Node.js 18+
- **Framework**: Express.js
- **API**: RESTful endpoints for cart operations

### Testing Stack
- **Unit Testing**: Vitest, React Testing Library
- **E2E Testing**: Selenium WebDriver (Python)
- **BDD Framework**: Behave (Python's Cucumber equivalent)
- **Gherkin**: Feature files for behavior specification
- **CI/CD Testing**: Azure Playwright Testing (cloud execution)
- **Pattern**: Page Object Model (POM)

### AI & Development Tools
- **GitHub Copilot**: AI-powered code completion
- **Copilot Chat**: Interactive AI assistant
- **Copilot Agent Mode**: Autonomous code generation
- **Spec Kit**: Technical planning and task breakdown
- **Foundry Agent**: Test scenario generation
- **Copilot Custom Agent**: Test script generation
- **GitHub MCP**: Model Context Protocol for GitHub integration

### DevOps & CI/CD
- **Version Control**: Git, GitHub
- **CI/CD**: GitHub Actions
- **Cloud Testing**: Azure Playwright Testing
- **Notifications**: Slack, Microsoft Teams integration
- **Reporting**: Test result dashboards

## ⏱️ Time Commitment

### Exercise 1: Development Persona
- **Phase 1**: Knowledge Ingestion & Requirement Enrichment - *Hands-on workshop time*
- **Phase 2**: Technical Planning & Scaffolding - *Hands-on workshop time*
- **Phase 3**: Agentic Implementation - **3-4 hours**
- **Feature Implementation Estimate**: 10-12 hours (8 story points)

### Exercise 2: Testing Persona  
- **Phase 1**: Test Scenario Generation - **2.5-3 hours**
- **Phase 2**: Automation Scripting (Selenium + Behave BDD) - **3.5-4 hours**
- **Phase 3**: CI/CD Integration (Azure Playwright) - **3.5-4.5 hours**
- **Total Exercise 2**: **9.5-11.5 hours**

**Note**: Exercise 1 Phases 1 & 2 are primarily guided learning experiences. The time estimates focus on hands-on implementation work.

## 📖 Documentation

- **[WORKSHOP_SUMMARY.md](./WORKSHOP_SUMMARY.md)**: Comprehensive high-level overview of all workshop content
- **Workshop Instructions**: Located in `Workshop-AI-SDLC/` directory

## 🎓 Learning Outcomes

### Development Skills (Exercise 1)
- ✅ **AI-Assisted Analysis**: Use Copilot to analyze brownfield applications and identify feature gaps
- ✅ **Requirement Engineering**: Enrich functional and non-functional requirements with AI assistance
- ✅ **Technical Planning**: Create design guardrails and use Spec Kit for task breakdown
- ✅ **Autonomous Development**: Leverage Copilot Agent Mode for autonomous code generation
- ✅ **React Patterns**: Master Context API for state management and localStorage persistence
- ✅ **Component Architecture**: Build reusable, accessible components with TypeScript
- ✅ **Accessibility**: Implement WCAG 2.1 Level AA compliance (ARIA labels, keyboard navigation)
- ✅ **Testing**: Write unit and integration tests with 80%+ coverage
- ✅ **Git Workflows**: Professional PR management with AI-generated summaries

### Testing & QA Skills (Exercise 2)
- ✅ **Test Design**: Use Foundry Agent to generate 100+ comprehensive test scenarios
- ✅ **Test Coverage**: Create coverage matrix mapping requirements to test cases
- ✅ **BDD Automation**: Implement Behavior-Driven Development with Behave and Gherkin
- ✅ **Selenium WebDriver**: Build robust test automation with Python
- ✅ **Design Patterns**: Apply Page Object Model (POM) for maintainable tests
- ✅ **Multi-Browser Testing**: Configure cross-browser test execution
- ✅ **CI/CD Integration**: Setup GitHub Actions and Azure Playwright Testing
- ✅ **Cloud Testing**: Execute tests in Azure cloud environment
- ✅ **DevOps**: Configure notifications, reporting, and scheduled test runs

### Cross-Cutting Skills
- ✅ **AI Collaboration**: Effectively guide and review AI-generated code
- ✅ **Documentation**: Create comprehensive technical documentation
- ✅ **Problem Solving**: Debug issues in brownfield applications
- ✅ **Quality Assurance**: Balance speed with code quality and test coverage

## 💻 Prerequisites

### Required Software
- **Visual Studio Code** with GitHub Copilot extension
- **GitHub account** with Copilot access enabled
- **Node.js** 18+ and npm
- **Python** 3.9+ (for Exercise 2 test automation)
- **Git** installed and configured
- **Web Browsers**: Chrome, Firefox, or Edge (for testing)

### Required Knowledge
- **JavaScript/TypeScript basics** (variables, functions, async/await)
- **React fundamentals** (components, props, hooks) - for Exercise 1
- **HTML/CSS basics** for understanding web structure
- **Git basics** (clone, commit, push, pull)
- **Testing concepts** (test cases, assertions) - for Exercise 2

### Optional but Helpful
- Experience with brownfield/legacy applications
- Understanding of REST APIs
- Familiarity with BDD (Behavior-Driven Development)
- Knowledge of CI/CD pipelines
- Azure account (free tier works for Exercise 2, Phase 3)

### Accounts & Access
- **GitHub**: Repository access and Copilot subscription
- **Azure** (Optional): Free tier for cloud test execution in Exercise 2, Phase 3

## 🔗 Repository

**GitHub**: [CanarysPlayground/ai-sdlc-brownfield-workshop](https://github.com/CanarysPlayground/ai-sdlc-brownfield-workshop)

## 🤝 Getting Help

If you encounter issues during the workshop:
1. Review the detailed phase instructions
2. Check the [WORKSHOP_SUMMARY.md](./WORKSHOP_SUMMARY.md) for context
3. Refer to troubleshooting sections in each phase

---

**Ready to start?** Begin with [Exercise 1, Phase 1: Knowledge Ingestion & Requirement Enrichment](./Workshop-AI-SDLC/Exercise%201/1.%20Enrich-requirement.md)

Happy Learning! 🚀
