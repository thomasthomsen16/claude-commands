---
description: Automatically generates technical and user documentation for new features
---

# Document Feature Command

This command analyzes a feature implementation and generates both technical documentation for developers and user-friendly guides for end users.

## Usage
```
/document-feature <feature-name>
```

## Parameters
- `feature-name`: The name of the feature to document (e.g., "password-reset", "user-profile", "payment-integration")

## What this command does

1. **Analyzes the codebase** to find files related to the specified feature
2. **Detects feature type** (frontend, backend, or full-stack) based on file patterns
3. **Generates technical documentation** with:
   - API endpoints and specifications
   - Implementation details
   - Code architecture notes
   - Dependencies and integrations
4. **Creates user documentation** with:
   - Step-by-step instructions
   - Screenshot placeholders
   - Troubleshooting tips
   - Cross-references to related features

## Output
The command creates two documentation files:
- `docs/dev/{feature-name}-implementation.md` - Technical documentation
- `docs/user/how-to-{feature-name}.md` - User guide

## Your task

1. First, search the codebase for files related to the feature name using patterns like:
   - File names containing the feature name
   - Function/class names with the feature name
   - API routes related to the feature
   - Component names matching the feature

2. Analyze the found files to determine:
   - Feature type (frontend/backend/full-stack)
   - Main entry points and workflows
   - API endpoints and data models
   - User-facing components and flows

3. Create the docs/ directory structure if it doesn't exist:
   - docs/dev/ for technical documentation
   - docs/user/ for user guides

4. Generate technical documentation including:
   - **Overview**: Brief description of the feature
   - **Architecture**: How the feature fits into the overall system
   - **API Reference**: Endpoints, request/response formats, authentication
   - **Implementation Details**: Key functions, classes, and algorithms
   - **Database Schema**: Tables, relationships, indexes (if applicable)
   - **Dependencies**: External libraries, services, or APIs used
   - **Testing**: How to test the feature
   - **Deployment**: Special deployment considerations

5. Generate user documentation including:
   - **Introduction**: What the feature does and why it's useful
   - **Getting Started**: Prerequisites and setup steps
   - **Step-by-Step Guide**: Detailed instructions with screenshot placeholders
   - **Common Use Cases**: Examples of how to use the feature
   - **Troubleshooting**: Common issues and solutions
   - **FAQ**: Frequently asked questions
   - **Related Features**: Links to other relevant documentation

6. For screenshot placeholders in user docs, use this format:
   ```markdown
   ![Screenshot description](./screenshots/{feature-name}-step-{number}.png)
   *Screenshot: Brief description of what should be shown*
   ```

7. Add cross-references between technical and user documentation:
   - Link from user docs to relevant technical sections
   - Reference user workflows in technical implementation notes

8. If existing documentation structure is found, follow those patterns and conventions.

## Example Output Structure

For a "password-reset" feature, generate:

**docs/dev/password-reset-implementation.md**:
```markdown
# Password Reset - Technical Implementation

## Overview
Technical implementation of the password reset functionality...

## API Endpoints
### POST /api/auth/forgot-password
...

## Implementation Details
...
```

**docs/user/how-to-reset-password.md**:
```markdown
# How to Reset Your Password

## Introduction
This guide shows you how to reset your password if you've forgotten it...

## Steps
1. Navigate to the login page
   ![Login page](./screenshots/password-reset-step-1.png)
   *Screenshot: Show the login page with "Forgot Password" link highlighted*
...
```

Remember to:
- Use clear, consistent formatting
- Include code examples where relevant
- Add proper markdown headers for navigation
- Cross-reference related documentation
- Follow any existing documentation style in the project