# Installation Guide

This guide will walk you through the process of installing and setting up Cursor Project Rules in your project.

## Prerequisites

Before you begin, make sure you have:

- [Cursor Editor](https://cursor.sh) installed on your machine
- A project where you want to use the AI assistance
- Git installed (for cloning the repository)

## Installation Methods

There are two main ways to add Cursor Project Rules to your project:

### Method 1: Clone and Copy (Recommended)

This method gives you a local copy of the entire repository, which you can reference and update as needed.

1. Clone the repository to your local machine:

```bash
git clone https://github.com/VidAIze/best-cursor-project-rules.git
```

2. Copy the `.cursor` folder to your project:

```bash
cp -r best-cursor-project-rules/.cursor /path/to/your/project/
```

3. Restart Cursor or reload your project to apply the changes.

### Method 2: Direct Download

If you just want the rules without cloning the entire repository:

1. Download the repository as a ZIP file from GitHub:

   - Visit [https://github.com/VidAIze/best-cursor-project-rules](https://github.com/VidAIze/best-cursor-project-rules)
   - Click the "Code" button and select "Download ZIP"

2. Extract the ZIP file on your computer

3. Copy the `.cursor` folder to your project root:

```bash
cp -r best-cursor-project-rules-main/.cursor /path/to/your/project/
```

4. Restart Cursor or reload your project to apply the changes.

## Verification

To verify that the rules are properly installed:

1. Open your project in Cursor
2. Create a new file or open an existing one
3. Ask Cursor AI about one of the documented frameworks, for example:
   - "How do I set up a chat interface with the AI SDK and OpenAI?"
   - "How can I implement Clerk authentication in my app?"

If the AI provides detailed, accurate responses based on the documentation, the rules are working correctly.

## Selective Installation

If you only need specific rules rather than all of them, you can selectively copy only the rules you need:

```bash
# Create the rules directory if it doesn't exist
mkdir -p /path/to/your/project/.cursor/rules

# Copy only specific rules
cp best-cursor-project-rules/.cursor/rules/01-openai.mdc /path/to/your/project/.cursor/rules/
cp best-cursor-project-rules/.cursor/rules/clerk-guide.mdc /path/to/your/project/.cursor/rules/
# And so on for other rules you need
```

## Troubleshooting

If the rules don't seem to be working:

1. Ensure the `.cursor` folder is at the root of your project
2. Check that the rule files have the `.mdc` extension
3. Restart Cursor completely (not just reload the project)
4. Verify you're asking about technologies covered by the installed rules

## Updating

To update to the latest version of the rules:

1. Pull the latest changes if you cloned the repository:

```bash
cd path/to/best-cursor-project-rules
git pull
```

2. Copy the updated `.cursor` folder to your project again.

## Next Steps

Now that you have installed Cursor Project Rules, check out the [Usage Examples](Usage-Examples) to learn how to make the most of them.
