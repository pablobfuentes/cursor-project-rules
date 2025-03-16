# Rule Formats

This page explains the structure and format of Cursor Project Rules files, which are used to provide documentation to the Cursor AI.

## Basic Structure

Cursor Project Rules are stored as Markdown files with the `.mdc` extension in the `.cursor/rules` directory of your project. Each rule file provides documentation for a specific framework, library, or tool.

## File Naming Conventions

Rules follow these naming conventions:

- For general framework documentation: `framework-name.mdc` (e.g., `nextjs.mdc`)
- For numbered sequence of related docs: `##-name.mdc` (e.g., `01-openai.mdc`, `02-anthropic.mdc`)
- For usage-specific documentation: `name-usage.mdc` (e.g., `shadcn-usage.mdc`)

## Rule File Structure

A typical rule file follows this structure:

````markdown
# Title of Documentation

A brief description of the framework and its purpose.

## Section 1

Content for the first section, which might include:

- Bullet points
- Code examples
- Explanation text

## Section 2

Content for the second section.

### Subsection

More detailed information in a subsection.

## Examples

```jsx
// Code examples are particularly useful
function Example() {
  return <div>Example component</div>;
}
```
````

## Next Steps or Related Information

Additional guidance or links to related topics.

````

## Required Elements

Every rule file should include:

1. **Title**: A clear, descriptive title at the top
2. **Overview**: A brief description of what the rule covers
3. **Structured Sections**: Logical divisions of the content
4. **Code Examples**: Where appropriate, with correct syntax highlighting
5. **Practical Examples**: Real-world usage scenarios

## Best Practices for Rule Creation

When creating or modifying rules:

1. **Be Comprehensive**: Cover all important aspects of the framework
2. **Stay Current**: Keep information up-to-date with the latest versions
3. **Use Clear Language**: Write in simple, direct terms
4. **Include Examples**: Provide practical code samples
5. **Document Errors**: Include common errors and their solutions
6. **Consider Use Cases**: Address the most common use cases
7. **Keep It Reasonable**: Aim for 2-25KB per file (not too small, not too large)

## Example Rule: Simple Example

Here's a simple example of a rule file for a fictional UI library:

```markdown
# SimpleUI Documentation

SimpleUI is a lightweight UI library for React applications, designed to provide basic components with minimal styling.

## Installation

```bash
npm install simple-ui-react
````

## Basic Usage

Import components from the library:

```jsx
import { Button, Card } from "simple-ui-react";

function MyComponent() {
  return (
    <Card>
      <h2>Hello World</h2>
      <Button onClick={() => alert("Clicked!")}>Click Me</Button>
    </Card>
  );
}
```

## Components

### Button

The Button component provides a clickable button element with basic styling.

Props:

- `variant`: 'primary' | 'secondary' | 'ghost' (default: 'primary')
- `size`: 'small' | 'medium' | 'large' (default: 'medium')
- All standard button HTML attributes

### Card

A container component with elevation and padding.

Props:

- `elevation`: 0-5 (default: 1)
- `padding`: 'none' | 'small' | 'medium' | 'large' (default: 'medium')

````

## Example Real Files

For reference, you can look at these existing rule files in the repository:

- `01-openai.mdc`: Documentation for the OpenAI API
- `clerk-guide.mdc`: Guide for integrating Clerk authentication
- `shadcn-usage.mdc`: Usage guide for shadcn/ui components

## Creating Your Own Rules

To create your own rule:

1. Create a new `.mdc` file in the `.cursor/rules` directory
2. Follow the format outlined above
3. Ensure the content is accurate and comprehensive
4. Test the rule by asking the Cursor AI questions about the documented framework

See [Creating New Rules](Creating-New-Rules) for a more detailed guide on creating custom rules.

## Advanced Rule Features

### Categorization and Discoverability

You can make your rules more discoverable by:

1. Using clear, searchable titles and section headers
2. Including common terms and synonyms for key concepts
3. Cross-referencing related rules with mentions

### Versioning Information

If documenting a framework with multiple versions, clearly indicate version-specific features:

```markdown
## Feature X (v2.0+)

This feature is only available in version 2.0 and above.

## Legacy Feature Y (deprecated in v3.0)

This feature is deprecated and will be removed in future versions.
````

## Next Steps

After understanding rule formats, learn how to create your own custom rules in [Creating New Rules](Creating-New-Rules).
