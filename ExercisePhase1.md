# Workshop 1: Development Persona – Phase 1
## Knowledge Ingestion & Requirement Enrichment

---

## 📋 **OVERVIEW**

**Workshop**: Development Persona – Requirement to Code  
**Phase**: 1 of 3 (Knowledge Ingestion & Requirement Enrichment)  


### **Scenario**
You are a developer working on the **OctoCAT Supply Chain Management** system, a brownfield application for managing cat-related products. Users report that clicking on "Products" from the home page displays a loading spinner, then shows **"Failed to fetch products"** error message.

Your task is to:
1. Aggregate existing technical documentation (TDD, HLD, requirements)
2. Use GitHub Copilot to analyze the codebase and identify root causes
3. Use Copilot to enrich requirements with missing specifications
4. Create a comprehensive GitHub Issue with the enriched functional specifications

### **Learning Objectives**
By completing Phase 1, you will learn to:
- ✅ Build a knowledge repository from existing documentation and code
- ✅ Use GitHub Copilot Chat to analyze brownfield applications
- ✅ Leverage AI to identify missing requirements and enrich specifications
- ✅ Use GitHub MCP to programmatically create detailed GitHub Issues
- ✅ Document requirements in a structured, actionable format

---

## 🎯 **PREREQUISITES**

### **Required Tools**
- ✅ Visual Studio Code with GitHub Copilot extension
- ✅ GitHub Copilot Chat enabled
- ✅ GitHub MCP (Model Context Protocol) configured
- ✅ Git installed and configured
- ✅ Node.js 18+ and npm installed


### **Repository Setup**
- Clone the workshop repository:
  ```bash
  git clone https://github.com/CanarysPlayground/ai-sdlc-brownfield-workshop.git
  cd ai-sdlc-brownfield-workshop/supply-chain-system
  ```

---

## 🚀 **PHASE 1: KNOWLEDGE INGESTION & REQUIREMENT ENRICHMENT**

---

### **STEP 1: REPRODUCE THE ISSUE** (10 minutes)

#### 1.1 Start the Application

**Start the API Server:**
```bash
cd supply-chain-system/api
npm install
npm run dev
```

**Expected Output:**
```
Server running on http://localhost:3000
Database initialized successfully
```

**Start the Frontend:**
Open a new terminal:
```bash
cd supply-chain-system/frontend
npm install
npm run dev
```

**Expected Output:**
```
VITE ready in 500ms
Local: http://localhost:5173/
```

#### 1.2 Reproduce the Error

1. Open browser: `http://localhost:5173/`
2. Click **"Explore Products"** button on home page
3. **Observe**: Loading spinner appears
4. **Observe**: Error message displays: **"Failed to fetch products"**

#### 1.3 Check Browser Console

Open Developer Tools (F12) → Console tab

**Expected Error:**
```
Failed to fetch products
Error: Network Error or API Error
```

#### 1.4 Document Initial Observations

Create a new file for tracking:
```bash
mkdir -p docs/investigation
touch docs/investigation/issue-analysis.md
```

Add initial observations:
```markdown
# Product Page Load Issue - Initial Analysis

## Issue Description
- **Symptom**: Products page shows loading spinner then "Failed to fetch products" error

## Initial Questions
1. Is the API server running?
2. Is the API endpoint correct?
3. Are there CORS issues?
4. Is the database initialized?
5. Are there authentication requirements?
```

---

### **STEP 2: BUILD KNOWLEDGE REPOSITORY** (20 minutes)

#### 2.1 Aggregate Existing Documentation

Use GitHub Copilot Chat to extract existing documentation:

**Prompt 1: Extract Architecture Overview**
```
@workspace Analyze the supply-chain-system codebase and create a High-Level Design (HLD) document.

Include:

1. **System Architecture**
   - Frontend architecture (React, TypeScript, Vite)
   - Backend architecture (Express, Node.js)
   - Database (SQLite)
   - API design patterns

2. **Component Structure**
   - Frontend components hierarchy
   - Backend routes and repositories
   - Database models

3. **Technology Stack**
   - Frontend: React version, UI libraries, state management
   - Backend: Express version, middleware
   - Database: SQLite version, ORM/query approach

4. **Data Flow**
   - User clicks Products → Frontend request → API endpoint → Database → Response
   - Where could failures occur?

5. **Existing Product Feature**
   - Current implementation of Products.tsx
   - API endpoint: /api/products
   - Repository: ProductsRepository
   - Database table: products

Focus on files:
- frontend/src/components/entity/product/Products.tsx
- api/src/routes/product.ts
- api/src/repositories/productsRepo.ts
- api/src/models/product.ts

Create a comprehensive HLD document.
```

**Save Output:**
- Create: `docs/knowledge-repository/high-level-design.md`
- Paste Copilot's response

#### 2.2 Extract Technical Design Details

**Prompt 2: Create Technical Design Document (TDD)**
```
@workspace Create a Technical Design Document (TDD) for the Products feature.

Based on:
- frontend/src/components/entity/product/Products.tsx
- frontend/src/api/config.ts
- api/src/routes/product.ts
- api/src/repositories/productsRepo.ts
- api/src/db/sqlite.ts

Include:

1. **Component Design: Products.tsx**
   - State management (useState, useQuery)
   - Data fetching strategy (react-query)
   - Error handling approach
   - Loading states
   - Props and interfaces

2. **API Design: /api/products**
   - Endpoint: GET /api/products
   - Request format
   - Response format
   - Error responses
   - CORS configuration

3. **Repository Pattern: ProductsRepository**
   - Database connection
   - Query methods (findAll, findById, create, update, delete)
   - Error handling
   - Transaction management

4. **Database Schema: products table**
   - Table structure
   - Columns and types
   - Indexes
   - Foreign keys

5. **Current Implementation Issues**
   - Identify potential error points
   - Missing error handling
   - Configuration issues

Provide detailed technical specifications.
```

**Save Output:**
- Create: `docs/knowledge-repository/technical-design-document.md`
- Paste Copilot's response

#### 2.3 Document Current Requirements

**Prompt 3: Extract Current Product Requirements**
```
@workspace Analyze the Products feature and document the current requirements.

Based on:
- frontend/src/components/entity/product/Products.tsx
- Existing functionality
- User interactions
- API contracts

Create a requirements document with:

1. **Functional Requirements**
   - FR-1: Display list of all products
   - FR-2: Search products by name/description
   - FR-3: View product details in modal
   - FR-4: Add products to cart (TODO)
   - FR-5: Responsive design
   - FR-6: Dark mode support

2. **Non-Functional Requirements**
   - NFR-1: Page load time < 2 seconds
   - NFR-2: Handle API errors gracefully
   - NFR-3: Accessible (WCAG 2.1 Level AA)
   - NFR-4: Mobile-first responsive

3. **Current User Stories**
   - As a user, I want to view all products so I can browse the catalog
   - As a user, I want to search products so I can find specific items
   - As a user, I want to see product details so I can make informed decisions

4. **Acceptance Criteria**
   For "View All Products" story:
   - [ ] Products load on page navigation
   - [ ] Display product image, name, description, price
   - [ ] Show loading state while fetching
   - [ ] Display error message on failure
   - [ ] Support dark mode

List all current requirements and identify gaps.
```

**Save Output:**
- Create: `docs/knowledge-repository/current-requirements.md`
- Paste Copilot's response

#### 2.4 Organize Knowledge Repository

Your knowledge repository structure should look like:
```
docs/
└── knowledge-repository/
    ├── high-level-design.md          # System architecture
    ├── technical-design-document.md  # Technical specifications
    ├── current-requirements.md       # Existing requirements
    └── README.md                     # Knowledge repo index
```


## Documents
1. **[High-Level Design](./high-level-design.md)** - System architecture and component overview
2. **[Technical Design Document](./technical-design-document.md)** - Detailed technical specifications
3. **[Current Requirements](./current-requirements.md)** - Functional and non-functional requirements

## Usage
These documents serve as the knowledge base for:
- Understanding the existing system
- Identifying missing requirements
- Planning enhancements
- Guiding AI agents during code generation




---

### **STEP 3: USE COPILOT TO ANALYZE & IDENTIFY ROOT CAUSE** 

#### 3.1 Perform Systematic Analysis

**Prompt 4: Analyze Products.tsx Component**
```
@workspace Analyze frontend/src/components/entity/product/Products.tsx for the 
"Failed to fetch products" error.

Investigate:

1. **Data Fetching**
   - How is fetchProducts() implemented?
   - What API endpoint is called?
   - What is the full URL being requested?
   - Check api.baseURL and api.endpoints.products in frontend/src/api/config.ts

2. **Error Handling**
   - What error states exist?
   - How are errors caught and displayed?
   - What information is lost in error handling?

3. **API Configuration**
   - Is the API base URL correct?
   - Are there environment variables needed?
   - CORS configuration?

4. **Dependencies**
   - React Query configuration
   - Axios configuration
   - Any interceptors or middleware?

Provide:
- Root cause hypothesis
- Evidence from code
- Suggested fixes
```

**Prompt 5: Analyze Backend API Endpoint**
```
@workspace Analyze api/src/routes/product.ts and related files for the 
products API endpoint.

Investigate:

1. **Route Registration**
   - Is the /api/products route registered in api/src/index.ts?
   - Correct HTTP method (GET)?
   - Any middleware that might block requests?

2. **Database Connection**
   - Is the database initialized in init-db.ts?
   - Are migrations run successfully?
   - Is seed data loaded?

3. **Error Handling**
   - How are errors caught in the route handler?
   - Are errors properly serialized?
   - Status codes correct?

4. **Repository Implementation**
   - Check productsRepo.ts findAll() method
   - Database query correctness
   - Error handling in repository layer

Provide detailed analysis with code references.
```

**Prompt 6: Check API Configuration & CORS**
```
@workspace Check API configuration for CORS and connectivity issues.

Analyze:

1. **CORS Configuration** (api/src/index.ts)
   - Is CORS enabled?
   - Are origins configured correctly?
   - Does localhost:5173 have access?

2. **API Base URL** (frontend/src/api/config.ts)
   - Is base URL pointing to correct port (3000)?
   - Is protocol correct (http vs https)?
   - Any proxy configuration?

3. **Port Configuration**
   - Frontend runs on: 5173
   - API should run on: 3000
   - Are these ports configured correctly?

4. **Environment Variables**
   - Check .env files
   - Runtime configuration
   - Default values

Identify configuration mismatches that could cause connection failures.
```

#### 3.2 Document Root Cause Analysis

Update `docs/investigation/issue-analysis.md`:

```markdown
## Root Cause Analysis (from Copilot)

### Findings:

1. **API Configuration Issue**
   - [Paste Copilot's findings about API config]
   - Evidence: [Code references]

2. **CORS Configuration Issue**
   - [Paste Copilot's findings about CORS]
   - Evidence: [Code references]

3. **Database Initialization Issue**
   - [Paste Copilot's findings about DB]
   - Evidence: [Code references]

### Hypothesis:
[Based on analysis, state the most likely root cause]

### Evidence:
- Code file: [file path]
- Line number: [line number]
- Issue: [specific problem]

### Verification Steps:
1. [How to verify this is the issue]
2. [What to check]
3. [Expected vs actual behavior]
```

---

### **STEP 4: IDENTIFY MISSING REQUIREMENTS** (15 minutes)

#### 4.1 Use Copilot to Identify Gaps

**Prompt 7: Identify Missing Requirements**
```
@workspace Based on the "Failed to fetch products" error and the analysis of 
the Products feature, identify missing requirements and specifications.

Context:
- Current issue: Products page fails to load
- Existing requirements in docs/knowledge-repository/current-requirements.md
- HLD in docs/knowledge-repository/high-level-design.md
- TDD in docs/knowledge-repository/technical-design-document.md

Identify missing:

1. **Error Handling Requirements**
   - Specific error scenarios (network, 404, 500, timeout)
   - User-facing error messages
   - Retry strategies
   - Fallback UI states

2. **API Reliability Requirements**
   - Response time SLAs
   - Timeout configurations
   - Retry logic
   - Circuit breaker patterns

3. **Logging & Monitoring Requirements**
   - Error logging (frontend & backend)
   - Performance monitoring
   - User analytics
   - Debug information

4. **Configuration Requirements**
   - Environment-specific configs
   - API endpoint configuration
   - CORS policies
   - Database connection settings

5. **Data Validation Requirements**
   - API response validation
   - Data type checking
   - Null/undefined handling
   - Schema validation

6. **User Experience Requirements**
   - Loading states
   - Empty states
   - Error recovery actions
   - Accessibility during errors

7. **Testing Requirements**
   - Unit tests for error scenarios
   - Integration tests for API calls
   - E2E tests for user flows
   - Error state testing

For each missing requirement, provide:
- Requirement ID
- Description
- Priority (High/Medium/Low)
- Rationale (why it's needed)
- Acceptance criteria

Structure as a formal requirements document.
```

**Save Output:**
- Create: `docs/knowledge-repository/missing-requirements.md`
- Paste Copilot's analysis


---

### **STEP 5: ENRICH REQUIREMENTS WITH AI** (20 minutes)

#### 5.1 Generate Comprehensive Requirements

**Prompt 8: Enrich Product Feature Requirements**
```
@workspace Create enriched, comprehensive requirements for fixing and enhancing 
the Products feature.

Based on:
- Root cause analysis in docs/investigation/issue-analysis.md
- Missing requirements in docs/knowledge-repository/missing-requirements.md
- Current requirements in docs/knowledge-repository/current-requirements.md

Generate a complete requirements specification that includes:

1. **Bug Fix Requirements**
   - Fix "Failed to fetch products" error
   - Specific technical solution
   - Configuration changes needed
   - Code changes required

2. **Enhanced Error Handling Requirements**
   - Network error handling
   - API error handling (400, 401, 403, 404, 500)
   - Timeout handling
   - Retry mechanism
   - User-friendly error messages
   - Error recovery actions (Retry button, Navigate home)

3. **Improved Loading States**
   - Skeleton loading UI
   - Progress indicators
   - Optimistic UI updates

4. **Enhanced User Experience**
   - Empty state when no products
   - Search improvements (debounce, clear button)
   - Product card enhancements
   - Modal improvements
   - Accessibility improvements

5. **Configuration Management**
   - Environment-based API URLs
   - Configurable timeouts
   - CORS configuration
   - Feature flags

6. **Logging & Monitoring**
   - Frontend error logging
   - Backend error logging
   - Performance metrics
   - User analytics events

7. **Testing Requirements**
   - Unit tests for components
   - API integration tests
   - E2E tests for user flows
   - Error scenario tests

For each requirement, provide:
- Requirement ID (e.g., BUG-FIX-001)
- Title
- Description
- User Story format: "As a [user], I want [goal], so that [benefit]"
- Acceptance Criteria (clear, testable)
- Technical Specifications (implementation details)
- Dependencies
- Priority (Critical/High/Medium/Low)
- Estimated Effort (Story Points or Hours)

Format as a professional Feature Requirements Document (FRD).
```

**Save Output:**
- Create: `docs/specifications/product-feature-requirements.md`
- Paste enriched requirements

---

**✅ Checkpoint**: Before proceeding, ensure:
- [ ] Root cause analysis documented
- [ ] Missing requirements identified and documented
- [ ] Feature requirements enriched with acceptance criteria
- [ ] All documentation saved in `docs/` folder
- [ ] Ready to create GitHub Issue

---

### **STEP 6: CONFIGURE GITHUB MCP** (15 minutes)

Before creating the GitHub Issue, you need to activate and configure GitHub MCP (Model Context Protocol) in VS Code.

#### What is GitHub MCP?

**Model Context Protocol (MCP)** is a standardized protocol that lets GitHub Copilot (especially Agent Mode) access structured tools such as:
- GitHub Issues, Pull Requests, and repository operations
- File operations and content access
- Custom local or remote tools
- Your own MCP servers for specialized functionality

MCP bridges the gap between AI assistants and your development environment, enabling programmatic access to GitHub and other services.

---

#### 6.1 Prerequisites

Before configuring the GitHub MCP Server, ensure you have:

✅ **GitHub Account**: Active GitHub account with access to the repo `ai-sdlc-brownfield-workshop`

✅ **Visual Studio Code**: Latest version installed

✅ **GitHub Copilot Enabled**: 
   - Copilot Business / Pro / Enterprise (if organization-controlled)
   - Active Copilot subscription

✅ **MCP Policy Enabled** (For Enterprise/Organization):
   - Ensure "MCP servers in Copilot" policy is enabled by your organization admins
   - Reference: [GitHub Docs](https://docs.github.com), [Microsoft Learn](https://learn.microsoft.com)

**Verify Prerequisites:**

1. Open VS Code
2. Check bottom-right corner for GitHub Copilot icon
3. Ensure you're signed into GitHub (bottom-left account icon)

---

#### 6.2 Enable MCP Server Marketplace in VS Code

**Step 1: Open Extensions Panel**
- Windows/Linux: `Ctrl+Shift+X`
- macOS: `Cmd+Shift+X`

**Step 2: Access MCP Server Filter**
1. Click the **Filter icon** in the Extensions panel (funnel icon, top-right)
2. Choose **MCP Server** from the dropdown

**Step 3: Enable MCP Marketplace** (First-time users)
- If this is your first time, VS Code will prompt you to enable the MCP Marketplace
- Click **Enable** when prompted
- VS Code will reload to activate MCP support

**Verification:**
- The MCP Server filter should now show available MCP servers in the marketplace

> 📚 **Reference**: [GitHub Docs - MCP Marketplace](https://docs.github.com)

---

#### 6.3 Install the GitHub MCP Server (Recommended Method)

This is the **official and easiest** way to configure GitHub MCP. It connects VS Code to GitHub's hosted MCP server—**no local runtime required**.

**Step 1: Search for GitHub MCP Server**

1. In the VS Code **Extensions search bar**, type:
   ```
   github mcp server
   ```

2. Locate **GitHub MCP Server** in the search results
   - Publisher: GitHub
   - Look for the official GitHub badge

**Step 2: Install the Server**

1. Click **Install** on the GitHub MCP Server extension
2. Wait for installation to complete
3. VS Code may prompt for permissions—grant them

**Step 3: Verify Installation**

1. Open **Command Palette**:
   - Windows/Linux: `Ctrl+Shift+P`
   - macOS: `Cmd+Shift+P`

2. Type and select:
   ```
   MCP: List Servers
   ```

3. You should see **`github`** listed as a configured server

**Expected Output:**
```
✅ github (remote) - Connected
```

> ✅ **Success!** You've connected VS Code to GitHub's hosted MCP server. No local runtime configuration needed.

> 📚 **Reference**: [GitHub Docs - GitHub MCP Server](https://docs.github.com)

---

#### 6.4 Enable Agent Mode (Required for MCP Tooling)

GitHub MCP is deeply integrated with **GitHub Copilot Agent Mode**. Agent Mode allows Copilot to use MCP tools directly (e.g., create issues, list branches, modify files).

**Step 1: Open VS Code Settings**

1. Open **Settings**:
   

2. In the search bar, type:
   ```
   chat.agent.enabled
   ```

**Step 2: Enable Agent Mode**

1. Locate the setting: **Chat: Agent Enabled**
2. Check the box to **turn on Agent Mode**

**Step 3: Verify Agent Mode**

1. Open **GitHub Copilot Chat**: `Ctrl+Shift+I` (or `Cmd+Shift+I` on Mac)
2. Type:
   ```
   @github help
   ```

**Expected Response:**
- Copilot should respond with available GitHub commands
- Examples: `create issue`, `list branches`, `show pull requests`, etc.

**If Agent Mode is not working:**
- Restart VS Code
- Ensure GitHub Copilot extension is up to date
- Check that you're signed into GitHub



#### 6.5 Verify MCP Setup and Test Connection

Before creating issues, verify that GitHub MCP is fully operational.

**Test 1: List Available Tools**

In **Copilot Chat**, type:
```
/tools list
```

**Expected Output:**
```
Available tools:
- @github: GitHub repository operations
  - create issue
  - list issues
  - show pull requests
  - search code
  [... more tools]
```

**Test 2: Test Repository Access**

In **Copilot Chat**, type:
```
@github Can you access the CanarysPlayground/ai-sdlc-brownfield-workshop repository?
```

**Expected Response:**
- ✅ Copilot confirms it can access the repository
- May show repository information (branches, recent commits, issues)

**Test 3: List Open Issues** (Simple Query)

```
@github List the open issues in CanarysPlayground/ai-sdlc-brownfield-workshop
```

**Possible Responses:**

✅ **Success:**
```
Found X open issues:
- Issue #Y: [Title]
- Issue #Z: [Title]
```
or
```
No open issues found in this repository.
```
→ **MCP is working! Proceed to Step 7**

❌ **Error Scenarios:**

| Error Message | Solution |
|---------------|----------|
| "GitHub tools not available" | Go back to Step 6.2-6.3, reinstall GitHub MCP Server |
| "Authentication required" | Sign in to GitHub in VS Code (see Step 6.6) |
| "Repository not found" or "Access denied" | Verify repository URL and permissions (see Step 6.6) |
| "Agent mode not enabled" | Go back to Step 6.4, enable Agent Mode |

---

**✅ Checkpoint**: Before proceeding to Step 7, ensure:
- [ ] MCP Server Marketplace enabled in VS Code
- [ ] GitHub MCP Server installed (`MCP: List Servers` shows `github`)
- [ ] Agent Mode enabled (`chat.agent.enabled`)
- [ ] Authenticated with GitHub (signed in, bottom-left account icon)
- [ ] Repository access verified (`@github` responds to queries)
- [ ] Test query successful (repository information retrieved)

---

### **STEP 7: PREPARE & CREATE GITHUB ISSUE** (20 minutes)

Now that you've completed the analysis and GitHub MCP is configured, it's time to prepare a comprehensive GitHub Issue that consolidates all your findings and create it programmatically.



#### 7.1 Generate Issue Content Using Copilot

Use GitHub Copilot to consolidate all your documentation into a properly formatted GitHub Issue.

**Prompt 9: Generate Complete GitHub Issue Content**

```
@workspace Create a comprehensive GitHub Issue for fixing the Products page failure and enhancing error handling.

Consolidate information from all my documentation:
- docs/investigation/issue-analysis.md (root cause analysis)
- docs/knowledge-repository/missing-requirements.md (gap analysis)
- docs/specifications/product-feature-requirements.md (enriched requirements)
- docs/knowledge-repository/high-level-design.md
- docs/knowledge-repository/technical-design-document.md


Structure the GitHub Issue with these sections:

# Title
[BUG + ENHANCEMENT] Fix Products Page Load Failure & Enhance Error Handling

## 🐛 Bug Report

### Problem Description
- What: Products page shows "Failed to fetch products" error
- When: Users click "Explore Products" from home page
- Impact: Critical - users cannot browse or purchase products

### Steps to Reproduce
1. Start application (frontend :5173, API :3000)
2. Navigate to home page
3. Click "Explore Products" button
4. Observe loading spinner followed by error

### Expected vs Actual Behavior
- Expected: Products load in grid layout with images, names, prices, add-to-cart
- Actual: Loading spinner indefinitely, then error message

### Environment
- Frontend: React 18, TypeScript, Vite
- Backend: Node.js, Express, SQLite
- Repository: CanarysPlayground/ai-sdlc-brownfield-workshop/supply-chain-system

---

## 🔍 Root Cause Analysis

Extract and summarize findings from docs/investigation/issue-analysis.md:
- Primary issue identified
- Technical evidence (file, line, specific problem)
- Impact analysis (severity, scope, business impact)

---
## 📋 Requirements
**ENHANCE-002: Simple Skeleton Loading UI** 

User Story: As a user, I want to see placeholder cards while products load, so I know the page is working and have a sense of the layout.

Scope: Replace generic loading spinner with simple skeleton cards that match product card dimensions.

Acceptance Criteria:
- [ ] Display 6 skeleton cards in grid layout while loading
- [ ] Each skeleton shows placeholder for: image area, title area, price area
- [ ] Skeleton cards match the dimensions of actual ProductCard components
- [ ] Simple gray background with subtle pulse animation (CSS only)
- [ ] Skeleton is replaced by actual products when data loads
- [ ] Loading state announced to screen readers: "Loading products"

Technical Implementation:
- Create new component: `frontend/src/components/common/ProductSkeleton.tsx`
  - Simple functional component
  - Props: none (fixed at 6 cards)
  - Use divs with fixed heights to match ProductCard layout
  - CSS classes for gray background and pulse animation
- Modify `frontend/src/components/entity/product/Products.tsx`:
  - Import ProductSkeleton
  - Show ProductSkeleton when `isLoading === true`
  - Show products when data loaded
  - Show error message when error occurred
- Add simple CSS animation (pulse effect using keyframes)

Constraints:
- No complex animation libraries
- Fixed number of skeleton cards (6)
- Simple rectangular placeholders only
- Use CSS animations only (no JavaScript)

---


## 🛠️ Technical Specifications

### Files to Modify/Create

**1. `frontend/src/api/config.ts`** (MODIFY - Bug Fix)
- **Issue**: API base URL misconfigured
- **Changes**: 
  - Set correct API_BASE_URL: `http://localhost:3000/api`
  - Add timeout: 10 seconds
- **Effort**: 1 hour
- **Testing**: Verify API calls reach correct endpoint

**2. `frontend/src/components/entity/product/Products.tsx`** (MODIFY - Bug Fix + All Enhancements)
- **Current State**: Basic error handling, generic spinner
- **Changes**:
  - Import: ProductSkeleton, ErrorMessage, errorHandler
  - Add error state management
  - Replace spinner with ProductSkeleton when loading
  - Show ErrorMessage with retry button when error
  - Add retry handler function
  - Add console.error logging
- **Effort**: 8 hours
- **Testing**: Manual testing of all states (loading, success, error, retry)

**3. `frontend/src/api/errorHandler.ts`** (CREATE - ENHANCE-001)
- **Purpose**: Centralized error detection and messaging
- **Implementation**:
  ```typescript
  export function getErrorMessage(error: unknown): string {
    // Detect error type
    // Return user-friendly message
  }
  
  export function getErrorType(error: unknown): 'network' | 'server' | 'notfound' | 'generic' {
    // Simple error type detection
  }
  ```


## 📚 Documentation References
- Root Cause: `docs/investigation/issue-analysis.md`
- HLD: `docs/knowledge-repository/high-level-design.md`
- TDD: `docs/knowledge-repository/technical-design-document.md`
- Missing Reqs: `docs/knowledge-repository/missing-requirements.md`
- Feature Reqs: `docs/specifications/product-feature-requirements.md`

---



#### 7.4 Create GitHub Issue via MCP
**Prompt 10: Create GitHub Issue via MCP**

```
@github Create a new issue in the CanarysPlayground/ai-sdlc-brownfield-workshop repository with the following details:

Title: [BUG + ENHANCEMENT] Fix Products Page Load Failure & Enhance Error Handling

Body:
[Paste the complete issue content generated in Step 7.2 - the entire markdown from "# Title" to "Definition of Done"]

Labels: bug, enhancement, high-priority, frontend, backend, products, error-handling, ux-improvement
```

**Expected Response:**

```
✅ Issue created successfully!





### **🎉 CONGRATULATIONS! YOU'VE COMPLETED PHASE 1!**

**What You Accomplished:**

1. ✅ **Reproduced the Issue**: Understood the problem by observing the failing Products page
2. ✅ **Built Knowledge Repository**: Created comprehensive documentation using GitHub Copilot  
   - High-Level Design (HLD)
   - Technical Design Document (TDD)
   - Current Requirements
3. ✅ **Performed Root Cause Analysis**: Used AI to identify the technical issue causing the failure
4. ✅ **Identified Missing Requirements**: Conducted gap analysis to find what was missing
5. ✅ **Enriched Requirements**: Added detailed acceptance criteria, user stories, and technical specs
6. ✅ **Configured GitHub MCP**: Set up Model Context Protocol for programmatic GitHub operations
7. ✅ **Created Comprehensive Issue**: Generated and published a professional GitHub Issue with all findings

**Skills You Learned:**

✨ **AI-Powered Analysis**
- Using `@workspace` agent for documentation analysis
- Leveraging GitHub Copilot for root cause investigation
- AI-assisted requirement enrichment
- Prompt engineering for effective AI collaboration

✨ **Requirements Engineering**
- Identifying gaps in existing requirements
- Writing clear acceptance criteria
- Creating user stories
- Structuring technical specifications

✨ **GitHub MCP Configuration**
- Installing and configuring MCP servers
- Enabling Agent Mode
- Authenticating with GitHub
- Creating issues programmatically

✨ **Documentation Best Practices**
- Organizing knowledge repositories
- Writing professional GitHub Issues
- Structuring technical documentation
- Creating actionable definitions of done

**Your Documentation Assets:**

📁 **Investigation & Analysis:**
- `docs/investigation/issue-analysis.md` - Detailed root cause analysis

📁 **Knowledge Repository:**
- `docs/knowledge-repository/high-level-design.md` - System architecture
- `docs/knowledge-repository/technical-design-document.md` - Technical details
- `docs/knowledge-repository/current-requirements.md` - Existing requirements
- `docs/knowledge-repository/missing-requirements.md` - Gap analysis

📁 **Specifications:**
- `docs/specifications/product-feature-requirements.md` - Enriched requirements

📁 **GitHub Issue:**
- `docs/github-issue-draft.md` - Issue content backup
- `docs/github-issue-summary.md` - Issue metadata and summary
- **Live Issue**: https://github.com/CanarysPlayground/ai-sdlc-brownfield-workshop/issues/[YOUR-ISSUE-NUMBER]

**What's Next? 🚀**

**Phase 2 - Technical Planning (Workshop 1 - Part 2):**
- Use GitHub Copilot to create detailed implementation plan
- Break down the issue into subtasks
- Design component architecture
- Create test plans
- Use GitHub Spark for prototyping (optional)

**Phase 3 - Agentic Implementation (Workshop 1 - Part 3):**
- Use GitHub Copilot in Agentic Development Mode
- Implement bug fixes and enhancements
- Write tests
- Review and refine code
- Deploy and validate

**Your GitHub Issue is now ready to be used as the primary work item for Phase 2 and Phase 3!**


