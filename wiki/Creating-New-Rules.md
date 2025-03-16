# Creating New Rules

This guide explains how to create new rule files for the Cursor Project Rules repository. Custom rules allow you to provide additional documentation for frameworks and libraries that aren't already covered.

## Prerequisites

Before creating a new rule, make sure you:

1. Understand the [Rule Formats](Rule-Formats) and structure
2. Have in-depth knowledge of the framework/library you're documenting
3. Have access to the latest documentation for reference

## Step-by-Step Guide

### 1. Identify the Need

First, determine if a new rule is necessary:

- Check if the framework is already documented in the existing rules
- Consider if the framework is widely used and would benefit others
- Evaluate if the documentation is complex enough to warrant a rule

### 2. Plan Your Rule Structure

Before writing, outline the structure of your rule:

- Main sections and topics to cover
- Key concepts that need explanation
- Common use cases and examples
- Error scenarios and troubleshooting steps

### 3. Choose a Naming Convention

Follow these naming conventions:

- For general framework documentation: `framework-name.mdc` (e.g., `nextjs.mdc`)
- For numbered sequence of related docs: `##-name.mdc` (e.g., `03-cohere.mdc`)
- For usage-specific documentation: `name-usage.mdc` (e.g., `remix-usage.mdc`)

### 4. Create the Rule File

Create a new `.mdc` file in your local `.cursor/rules` directory:

```bash
touch .cursor/rules/your-framework-name.mdc
```

### 5. Write the Content

Write your rule content following the standard format:

````markdown
# Framework Name Documentation

A brief overview of the framework and what it's used for.

## Installation

```bash
npm install framework-name
```
````

## Basic Usage

Explain the fundamental usage patterns.

```jsx
// Code example
import { Component } from "framework-name";

function Example() {
  return <Component prop="value" />;
}
```

## Key Concepts

Explain important concepts and terminology.

## Common Patterns

Document frequently used patterns and best practices.

## API Reference

Document the main API components and their properties.

## Troubleshooting

Address common issues and their solutions.

````

### 6. Include Practical Examples

Always include practical, real-world examples:

- Simple starter examples
- More complex, realistic use cases
- Common integration scenarios

### 7. Test Your Rule

Test your rule to ensure it's working:

1. Save the file in your project's `.cursor/rules` directory
2. Restart Cursor or reload your project
3. Ask the Cursor AI questions related to your rule
4. Verify that the AI provides accurate information based on your documentation

### 8. Review and Refine

Review your rule for:

- Accuracy: Ensure all information is correct
- Clarity: Make sure explanations are clear and concise
- Comprehensiveness: Check that all important aspects are covered
- Examples: Verify that examples are practical and work as expected
- Formatting: Ensure Markdown formatting is correct

### 9. Contribute to the Repository

If you want to share your rule:

1. Fork the Cursor Project Rules repository
2. Add your rule file
3. Submit a pull request with a clear description of what your rule covers
4. Address any feedback from code reviews

## Best Practices

### Focus on Practical Information

- Prioritize practical usage over theoretical concepts
- Include code snippets for common tasks
- Document error messages and their resolutions

### Keep It Current

- Include version information for features
- Note deprecated or upcoming features
- Update rules when major framework versions are released

### Structure for Readability

- Use clear headings and sub-headings
- Break up long sections with examples or lists
- Use code blocks with appropriate language tags

### Avoid Duplication

- Don't repeat information already in other rules
- Reference other rules when appropriate
- Focus on unique aspects of your framework

## Example: Creating a Vue.js Rule

Here's a brief example of creating a Vue.js rule:

1. Create the file: `.cursor/rules/vuejs.mdc`

2. Write the content:

```markdown
# Vue.js Documentation

Vue.js is a progressive framework for building user interfaces. It is designed to be incrementally adoptable and can be used to power single-page applications.

## Installation

```bash
# npm
npm install vue@latest

# yarn
yarn add vue@latest

# pnpm
pnpm add vue@latest
````

## Basic Usage

Create a Vue application:

```js
import { createApp } from "vue";
import App from "./App.vue";

const app = createApp(App);
app.mount("#app");
```

## Component Syntax

Vue components can be written in Single-File Components (SFC) with a .vue extension:

```vue
<template>
  <div class="greeting">{{ message }}</div>
</template>

<script setup>
import { ref } from "vue";

const message = ref("Hello Vue!");
</script>

<style scoped>
.greeting {
  color: green;
  font-weight: bold;
}
</style>
```

## Composition API

Vue 3 introduced the Composition API for better code organization:

```js
import { ref, computed, onMounted } from "vue";

export default {
  setup() {
    // reactive state
    const count = ref(0);

    // computed property
    const doubleCount = computed(() => count.value * 2);

    // lifecycle hook
    onMounted(() => {
      console.log("Component mounted");
    });

    // expose to template
    return {
      count,
      doubleCount,
    };
  },
};
```

```

## Community Rule Standards

When contributing rules to the repository, we maintain these standards:

1. **Accuracy**: Information must be factually correct
2. **Neutrality**: Present information without bias
3. **Completeness**: Cover all major aspects of the framework
4. **Code Quality**: Ensure code examples follow best practices
5. **Attribution**: Credit sources where appropriate

## Next Steps

After creating your rule, consider:

- Creating additional rules for related frameworks
- Expanding existing rules with more examples
- Contributing your rules back to the main repository
```
