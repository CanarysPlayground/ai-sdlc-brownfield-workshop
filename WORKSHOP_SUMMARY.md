# AI-SDLC Brownfield Workshop - High-Level Summary

## Overview
This workshop teaches AI-assisted software development lifecycle (SDLC) practices on a brownfield application - the **OctoCAT Supply Chain Management System**. Participants learn how to leverage GitHub Copilot and AI agents throughout the entire development and testing lifecycle.

---

## Workshop Structure

The workshop is organized into **2 Main Exercises** covering different personas in the SDLC:

### Exercise 1: Development Persona (Requirement to Code)
**Goal**: Implement a complete cart icon feature from requirement enrichment to production-ready code

### Exercise 2: Testing Persona (Requirement to Test)  
**Goal**: Generate comprehensive test scenarios and automate testing for the implemented cart feature

---

## Exercise 1: Development Persona - Detailed Breakdown

### Phase 1: Knowledge Ingestion & Requirement Enrichment
**Estimated Time**: 2-3 hours

**What You'll Learn**:
- ✅ Analyze brownfield applications using GitHub Copilot Chat
- ✅ Build a knowledge repository from existing technical documentation
- ✅ Use AI to identify gaps in requirements (missing cart icon feature)
- ✅ Enrich functional specifications with AI assistance
- ✅ Create comprehensive GitHub Issues using GitHub MCP (Model Context Protocol)

**Key Activities**:
- Reproduce the cart icon issue in the application
- Aggregate existing documentation (TDD, HLD, requirements)
- Analyze frontend and backend gaps using Copilot
- Use AI to generate enriched requirements covering:
  - Functional requirements (cart icon, badge, notifications)
  - Non-functional requirements (performance, accessibility, dark mode)
  - Technical specifications (localStorage persistence, API integration)
- Create detailed GitHub Issue with acceptance criteria

**Deliverables**:
- Documentation folder with investigation analysis
- Knowledge repository with design documents
- Comprehensive GitHub Issue for cart icon feature

---

### Phase 2: Technical Planning & Scaffolding
**Estimated Time**: 2.5-3 hours

**What You'll Learn**:
- ✅ Use GitHub Copilot Spec Kit to break down issues into technical tasks
- ✅ Create design guardrails using `.github/instructions.md`
- ✅ Generate technical specifications for full-stack features
- ✅ Scaffold components following architectural patterns
- ✅ Create implementation milestones and task breakdowns

**Key Activities**:
- Review GitHub Issue from Phase 1
- Create design guardrails configuration (`.github/instructions.md`) covering:
  - Design system (colors, typography, spacing)
  - Component architecture patterns
  - State management guidelines
  - Coding standards and best practices
- Use Spec Kit to generate execution plans for:
  - Frontend: CartContext, CartIcon component, Header integration
  - Backend: Cart API endpoints, service layer, database schema
- Scaffold component structure with TypeScript types
- Create technical specifications and milestone documents

**Deliverables**:
- `.github/instructions.md` (design guardrails)
- Component scaffolding (CartContext, CartIcon with tests)
- Technical execution plans
- Implementation milestone documentation

---

### Phase 3: Agentic Implementation
**Estimated Time**: 3-4 hours

**What You'll Learn**:
- ✅ Use GitHub Copilot Agent Mode for autonomous code generation
- ✅ Monitor and guide AI agent implementation progress
- ✅ Implement complete features with AI assistance
- ✅ Write comprehensive tests with AI
- ✅ Create pull requests with AI-generated summaries
- ✅ Review and validate AI-generated code

**Key Activities**:
- **Implement CartContext** with localStorage persistence
  - Add/remove/update/clear cart operations
  - Derived state calculations (itemCount, total)
  - Error handling and validation
- **Implement CartIcon Component**
  - Shopping cart icon with dynamic badge
  - Badge displays item count (visible only when items > 0)
  - Accessibility (ARIA labels, keyboard navigation)
  - Dark mode support
- **Integrate Cart into Application**
  - Add CartIcon to Header component
  - Connect cart to Products page (Add to Cart functionality)
  - Implement toast notifications using react-hot-toast
  - Create Cart page with CRUD operations
- **Write Comprehensive Tests**
  - Unit tests for CartContext (>80% coverage)
  - Unit tests for CartIcon component
  - Integration tests for cart flows
- **Code Quality & Review**
  - Run linters and fix issues
  - Validate against design guardrails
  - Optimize with React.memo and useCallback
  - Perform accessibility and responsive design testing
- **Create Pull Request**
  - Generate commit messages with AI
  - Create comprehensive PR description
  - Self-review with Copilot
  - Link PR to original issue

**Deliverables**:
- Fully functional CartContext with persistence
- CartIcon component with badge
- Complete Cart page UI
- Comprehensive test suite
- Pull request ready for review

**Key Technical Concepts Covered**:
- React Context API for state management
- localStorage for client-side persistence
- Component composition and integration
- Toast notifications for user feedback
- Immutable state updates
- Performance optimization patterns
- WCAG 2.1 accessibility compliance
- Responsive design (mobile, tablet, desktop)

---

## Exercise 2: Testing Persona - Detailed Breakdown

### Phase 1: Test Scenario Generation & Planning
**Estimated Time**: 2.5-3 hours

**What You'll Learn**:
- ✅ Use Foundry Agent to analyze requirement documents
- ✅ Generate comprehensive test scenarios using AI
- ✅ Create structured test plans with preconditions and expected results
- ✅ Use GitHub MCP to create test-related GitHub Issues
- ✅ Map requirements to test coverage matrix

**Key Activities**:
- Analyze implemented cart icon feature from Workshop 1
- Use Foundry Agent to extract testable requirements
- Generate test scenarios covering:
  - **Functional Testing**: Add to cart, remove from cart, update quantities, cart persistence
  - **Non-Functional Testing**: Performance, accessibility, responsive design
  - **Edge Cases**: Empty cart, localStorage limits, invalid data
  - **Integration Testing**: End-to-end user flows
- Create test coverage matrix mapping requirements to test cases
- Document test data requirements
- Create GitHub Issues for test stories

**Deliverables**:
- Comprehensive test plan document
- Test case specifications
- Test coverage matrix
- GitHub Issues for test tracking

---

### Phase 2: Test Automation Script Generation
**Estimated Time**: 2.5-3 hours

**What You'll Learn**:
- ✅ Use Playwright Agent to generate automated test scripts
- ✅ Convert manual test cases to automated tests
- ✅ Implement page object model pattern
- ✅ Create reusable test utilities and fixtures
- ✅ Set up test configuration and environment

**Key Activities**:
- Set up Playwright testing framework
- Generate automated test scripts for:
  - Cart icon visibility and badge functionality
  - Add to cart workflows
  - Cart operations (add, remove, update, clear)
  - localStorage persistence testing
  - Accessibility testing (keyboard navigation, ARIA)
  - Responsive design testing
- Implement page object model for maintainability
- Create test data fixtures and helpers
- Configure test environments (CI/CD integration)

**Deliverables**:
- Playwright test automation suite
- Page object models
- Test configuration files
- Reusable test utilities

---

### Phase 3: Test Execution & Reporting
**Estimated Time**: 1.5-2 hours

**What You'll Learn**:
- ✅ Execute automated test suites
- ✅ Analyze test results and debug failures
- ✅ Generate test reports with AI assistance
- ✅ Create bug reports for failures
- ✅ Track test metrics and quality indicators

**Key Activities**:
- Execute full test suite across different browsers
- Run tests in different environments (dev, staging)
- Analyze test results and identify failures
- Debug failing tests with AI assistance
- Generate comprehensive test reports:
  - Pass/fail statistics
  - Code coverage metrics
  - Performance benchmarks
  - Accessibility compliance scores
- Create GitHub Issues for identified bugs
- Document test execution results

**Deliverables**:
- Test execution reports
- Bug reports (GitHub Issues)
- Coverage reports
- Quality metrics dashboard

---

## Key Technologies & Tools Used

### AI Tools:
- **GitHub Copilot**: AI-powered code completion and generation
- **GitHub Copilot Chat**: Interactive AI assistant for code analysis
- **GitHub Copilot Agent Mode**: Autonomous code implementation
- **Spec Kit**: Technical planning and task breakdown
- **Foundry Agent**: Test scenario generation and analysis
- **Playwright Agent**: Test automation script generation
- **GitHub MCP**: Model Context Protocol for GitHub integration

### Development Stack:
- **Frontend**: React, TypeScript, Vite, TailwindCSS
- **State Management**: React Context API
- **Persistence**: localStorage
- **Notifications**: react-hot-toast
- **Icons**: Heroicons
- **Backend**: Node.js, Express (API endpoints)
- **Testing**: Vitest, React Testing Library, Playwright
- **Version Control**: Git, GitHub

---

## Skills Mastered Across the Workshop

### AI-Assisted Development:
- Leveraging AI for requirement analysis and enrichment
- Using AI agents for autonomous code generation
- Guiding AI with design guardrails and specifications
- Reviewing and validating AI-generated code
- Iterative refinement with AI assistance

### Software Engineering:
- Requirements engineering in brownfield projects
- Technical planning and architecture design
- Component-driven development
- State management patterns (Context API)
- Test-driven development
- Code review and quality assurance

### Modern Development Practices:
- Git workflow and branch management
- Pull request creation and review process
- Continuous Integration/Continuous Deployment
- Documentation as code
- Accessibility-first development (WCAG 2.1)
- Responsive design principles
- Performance optimization

### Testing & Quality Assurance:
- Test scenario generation and planning
- Test automation with Playwright
- Unit, integration, and E2E testing
- Accessibility testing (keyboard navigation, screen readers)
- Cross-browser testing
- Test reporting and metrics

---

## Real-World Applications

This workshop teaches practices applicable to:
- **Legacy System Modernization**: Adding features to brownfield applications
- **AI-Augmented Development**: Accelerating development with AI tools
- **Full-Stack Development**: Frontend and backend integration
- **Quality Engineering**: Comprehensive testing strategies
- **DevOps**: CI/CD integration and automation
- **Accessibility Compliance**: WCAG 2.1 standards implementation

---

## Target Audience

### Development Persona (Exercise 1):
- Frontend developers learning React and TypeScript
- Backend developers working on API development
- Full-stack developers
- Developers new to AI-assisted coding
- Engineers working on brownfield/legacy systems

### Testing Persona (Exercise 2):
- QA Engineers and Testers
- Test Automation Engineers
- Developers responsible for testing
- Anyone learning AI-assisted test generation

---

## Prerequisites for Participants

### Technical Requirements:
- Visual Studio Code with GitHub Copilot extension
- GitHub account with Copilot access
- Node.js 18+ and npm
- Git installed and configured
- Basic JavaScript/TypeScript knowledge
- Familiarity with React (for Exercise 1)
- Understanding of testing concepts (for Exercise 2)

### Optional But Helpful:
- Experience with brownfield applications
- Knowledge of REST APIs
- Familiarity with Git workflows
- Understanding of accessibility standards

---

## Workshop Outcomes

By completing this workshop, participants will be able to:

✅ **Analyze and enhance brownfield applications** using AI tools  
✅ **Enrich requirements** with AI-assisted analysis  
✅ **Design and implement full-stack features** with AI guidance  
✅ **Write production-ready code** following best practices  
✅ **Create comprehensive test suites** using AI-generated scenarios  
✅ **Automate testing workflows** with modern tools  
✅ **Build accessible, responsive applications** that meet modern standards  
✅ **Use AI agents effectively** throughout the development lifecycle  
✅ **Create high-quality documentation** and GitHub Issues  
✅ **Follow professional Git workflows** with PR reviews  

---

## Time Investment

- **Exercise 1 (Development Persona)**: 7.5-10 hours total
  - Phase 1: 2-3 hours
  - Phase 2: 2.5-3 hours
  - Phase 3: 3-4 hours

- **Exercise 2 (Testing Persona)**: 6.5-8 hours total
  - Phase 1: 2.5-3 hours
  - Phase 2: 2.5-3 hours
  - Phase 3: 1.5-2 hours

**Total Workshop Time**: 14-18 hours

---

## Repository Information

**Repository**: [CanarysPlayground/ai-sdlc-brownfield-workshop](https://github.com/CanarysPlayground/ai-sdlc-brownfield-workshop)

**Workshop Materials Location**:
- Exercise 1 Instructions: `Workshop-AI-SDLC/Exercise 1/`
- Exercise 2 Instructions: `Workshop-AI-SDLC/Exercise 2/`

---

## Conclusion

This workshop provides hands-on experience with modern AI-assisted software development practices. Participants gain practical skills in leveraging GitHub Copilot and AI agents to accelerate development, improve code quality, and create comprehensive test coverage - all while working on a realistic brownfield application scenario.

The workshop emphasizes **learning by doing**, with each phase building on the previous one to create a complete, production-ready feature from requirements to tested implementation.
