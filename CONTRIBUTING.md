# Contributing to BlazeBite Documentation

> **Source of Truth:** These guidelines derive from `.github/copilot-instructions.md` (GitHub Copilot Space instructions). Reference that file for comprehensive standards and research rationale.

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

## Template Requirements

**Before creating ANY new documentation:**

1. **Check `templates/` directory** for applicable templates:
   - Setup/Onboarding → `templates/TEMPLATE_ONBOARDING.md`
   - Troubleshooting → `templates/TEMPLATE_TROUBLESHOOTING.md` (coming soon)
   - Feature Reference → `templates/TEMPLATE_FEATURE_REFERENCE.md` (coming soon)

2. **If template exists:** Follow it strictly
   - Replace all `[placeholders]`
   - Delete all `<!-- comments -->`
   - Complete quality checklist at bottom

3. **If no template exists:**
   - Follow core principles below
   - Consider creating template after 2-3 similar docs
   - Get @Inversity approval for new templates

**All docs must meet quality standards** whether templated or not (see Writing Style section).

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
- [ ] Validate against template quality checklist (if applicable)
- [ ] Confirm all `[placeholder]` text replaced
- [ ] All `<!-- comments -->` removed from template
