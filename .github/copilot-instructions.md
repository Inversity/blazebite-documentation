# Copilot Instructions for BlazeBite Documentation

## Repository Overview

This repository contains official documentation for BlazeBite venue onboarding, device setup, and operational procedures. The primary purpose is to provide clear, step-by-step guides for venue owners, support staff, and internal teams.

## Documentation Standards

### File Naming and Structure
- Use lowercase with hyphens for all markdown files: `tablet-setup.md`, `printer-bluetooth-setup.md`
- Be descriptive in file names - avoid generic names
- Follow the existing directory structure:
  ```
  blazebite-documentation/
  ├── onboarding/          # New venue setup guides
  ├── guides/              # Step-by-step procedures
  ├── troubleshooting/     # Problem resolution
  ├── internal/            # Staff-only procedures
  └── assets/              # Images, diagrams
  ```

### Writing Style Guidelines
- **Tense:** Always use present tense (e.g., "tap" not "tapped")
- **Steps:** Number all sequential steps clearly
- **Confirmations:** Include success confirmations after important steps
- **Troubleshooting:** Add troubleshooting sections for common failures
- **Clarity:** Write for non-technical users - use simple, clear language
- **Consistency:** Match the tone and structure of existing documentation

### Image Guidelines
- Store images in `/assets/images/[section]/`
- Use descriptive names: `portal-menu-setup-screen.png`
- Keep file sizes under 1MB when possible
- Always reference images with relative paths

### Markdown Formatting
- Use proper heading hierarchy (# for title, ## for main sections, ### for subsections)
- Use emojis sparingly and consistently with existing docs (✅, ⚠️, 💡, 📱, etc.)
- Use checklists for prerequisites and verification steps
- Use code blocks for technical information or configuration
- Use blockquotes or callout boxes for important warnings or tips

## Content Requirements

### For Setup Guides
1. Start with a "What's In Your Box" or "Prerequisites" section
2. Include time estimates for completion
3. Number all steps sequentially
4. Include verification steps after critical actions
5. Add troubleshooting sections for common issues
6. End with "Next Steps" or success confirmation

### For Reference Documentation
1. Begin with clear purpose statement
2. Include navigation overview for UI-based docs
3. Organize by feature or screen
4. Include practical examples
5. Document all options and settings

### For Troubleshooting Guides
1. Start with symptom description
2. List possible causes
3. Provide step-by-step resolution
4. Include escalation paths if resolution fails

## Testing Documentation

Before finalizing any documentation changes:
- Follow the guide yourself if possible
- Have someone else test the procedure
- Verify all internal links work
- Check that images display correctly
- Ensure formatting renders properly in markdown viewers

## Contributing Workflow

1. Create a descriptive branch name: `docs/updating-tablet-setup`
2. Make changes following the style guidelines above
3. Test procedures on actual devices when applicable
4. Keep changes focused and minimal
5. Reference existing documentation files (like CONTRIBUTING.md) for additional context

## Key Files to Reference
- `CONTRIBUTING.md` - Complete contribution guidelines
- `README.md` - Repository structure and quick links
- Existing documentation files for style and tone consistency

## Important Notes
- This is a documentation-only repository - no code or build processes
- Focus on clarity and accuracy over technical sophistication
- All documentation should be accessible to non-technical venue owners
- Internal procedures (in `/internal/`) may contain sensitive information
- Contact Joe Wayne for documentation issues or major changes
