# Contributing to BlazeBite Documentation

## Documentation Standards

### File Naming
- Use `UPPERCASE_WITH_UNDERSCORES.md` for all user-facing documentation
- Use `lowercase-with-hyphens.md` for model guides and internal tooling
- Be descriptive: `PRINTER_BLUETOOTH_SETUP.md` not `PRINTER.md`

### Writing Style
- Use present tense ("tap" not "tapped")
- Number all steps
- Include success confirmations
- Add troubleshooting for common failures
- Maximum 3 sentences per paragraph
- 6th grade reading level

### Documentation Structure
- **Onboarding guides** → `onboarding/` directory
- **Feature references** → `reference/` directory
- **Troubleshooting** → `troubleshooting/` directory
- **Daily operations** → `operational/` directory
- **Staff-only** → `internal/` directory
- **Templates** → `templates/` directory
- **Model guides** → `model-guides/` directory

### Images
- Store in `/assets/images/[section]/`
- Use descriptive names: `portal-menu-setup-screen.png`
- Keep under 1MB when possible

## Making Changes

1. Create a branch: `docs/updating-tablet-setup`
2. Check for existing templates in `templates/` directory
3. Make your changes following the appropriate template
4. Test procedures on actual devices
5. Submit PR with description of changes
6. Tag Joe for review

## Testing Documentation

Before submitting:
- [ ] Follow the guide yourself
- [ ] Have someone else test it
- [ ] Verify all links work (especially cross-folder references)
- [ ] Check images display correctly
- [ ] Validate against template checklist (if applicable)