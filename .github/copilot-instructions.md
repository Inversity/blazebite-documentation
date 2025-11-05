# Copilot Instructions for BlazeBite Documentation

## Repository Overview

This repository contains official documentation for BlazeBite venue onboarding, device setup, and operational procedures. The primary purpose is to provide clear, step-by-step guides for venue owners (cooks, cashiers, managers), support staff, and internal teams.

**Target Audience:** Non-technical venue staff in high-pressure environments (kitchens, stadiums, concessions). Documentation must be scannable, offline-friendly, and account for network failures.

---

## Repository Structure

```
blazebite-documentation/
│
├── templates/                         # Documentation templates (reusable patterns)
│   ├── TEMPLATE_ONBOARDING.md
│   ├── TEMPLATE_TROUBLESHOOTING.md
│   ├── TEMPLATE_FEATURE_REFERENCE.md
│   └── TEMPLATE_API_REFERENCE.md
│
├── model-guides/                      # AI model-specific optimization guides
│   ├── gpt5-documentation-guide.md
│   ├── gemini-documentation-guide.md
│   └── grok-documentation-guide.md
│
├── onboarding/                        # Setup guides for new venues/devices
│   ├── ONBOARDING_TABLET.md
│   ├── ONBOARDING_POS.md
│   ├── ONBOARDING_KIOSK.md
│   └── ONBOARDING_PORTAL.md
│
├── reference/                         # Feature documentation (how things work)
│   ├── KITCHEN_APP_REFERENCE.md
│   ├── PORTAL_REFERENCE.md
│   ├── CUSTOMER_APP_REFERENCE.md
│   └── HARDWARE_SPECIFICATIONS.md
│
├── troubleshooting/                   # Problem resolution guides
│   ├── PRINTER_TROUBLESHOOTING.md
│   ├── NETWORK_TROUBLESHOOTING.md
│   ├── APP_TROUBLESHOOTING.md
│   └── PORTAL_TROUBLESHOOTING.md
│
├── operational/                       # Day-to-day procedures
│   ├── DAILY_OPERATIONS.md
│   ├── MENU_MANAGEMENT.md
│   ├── REFUND_PROCEDURES.md
│   └── STAFF_TRAINING.md
│
├── internal/                          # Staff-only procedures (BlazeBite team)
│   ├── DEVICE_PROVISIONING.md
│   ├── VENUE_ONBOARDING.md
│   ├── SUPPORT_PROCEDURES.md
│   └── RELEASE_PROCESS.md
│
└── assets/                            # Images, diagrams, media
    ├── images/
    │   ├── onboarding/
    │   ├── troubleshooting/
    │   └── reference/
    ├── diagrams/
    └── logos/
```

---

## Documentation Standards

### File Naming Conventions

**Primary Documentation:**
- Use `UPPERCASE_WITH_UNDERSCORES.md` for all user-facing docs
- Examples: `ONBOARDING_TABLET.md`, `KITCHEN_APP_REFERENCE.md`, `PRINTER_TROUBLESHOOTING.md`

**Templates:**
- Format: `TEMPLATE_[TYPE].md`
- Examples: `TEMPLATE_ONBOARDING.md`, `TEMPLATE_TROUBLESHOOTING.md`

**Model-Specific Guides:**
- Use `lowercase-with-hyphens.md`
- Examples: `gpt5-documentation-guide.md`, `gemini-documentation-guide.md`

**Be descriptive** - Avoid generic names like `guide.md` or `setup.md`

---

### Writing Style Guidelines (Aligned with Space Instructions)

**Core Principles:**
- **Reading level:** 6th grade - venue staff under time pressure
- **Paragraph length:** Maximum 3 sentences per paragraph
- **Tense:** Present tense (e.g., "tap" not "tapped")
- **Voice:** Active only
- **Steps:** Single action per numbered step
- **Validation:** Include "You should see X" after major steps
- **Troubleshooting:** Inline (immediately after relevant step)
- **Escalation:** Clear "when to contact support" criteria

**Tone:**
- Skip pleasantries - get to substance
- Explain "why" for non-obvious steps
- Use concrete examples with exact button/screen labels
- Provide honest feedback about clarity/completeness

---

### Template Usage Guidelines

**Check for existing templates first:**

Before creating new documentation, review the `templates/` directory for applicable templates:

- **Setup/Onboarding Guides** → `templates/TEMPLATE_ONBOARDING.md`
- **Troubleshooting Guides** → `templates/TEMPLATE_TROUBLESHOOTING.md`
- **Feature Reference** → `templates/TEMPLATE_FEATURE_REFERENCE.md`
- **API Documentation** → `templates/TEMPLATE_API_REFERENCE.md`
- *(Additional templates may exist - check directory)*

**If a relevant template exists:**
- Follow it strictly to ensure consistency across similar documentation
- Use the template's quality checklist before publishing
- Reference the template in your PR description

**If no relevant template exists:**

1. **Create documentation following core principles:**
   - 6th grade reading level
   - Max 3 sentences per paragraph
   - Single-action steps with validation
   - Inline troubleshooting
   - See "Writing Style Guidelines" section

2. **After 2-3 similar docs exist, consider creating a template:**
   - Identify common structural patterns
   - Extract reusable elements
   - Document quality gates
   - Include inline usage instructions
   - Place in `templates/` directory with `TEMPLATE_` prefix

3. **Update this instructions file** to reference the new template

**Creating New Templates:**
- Use existing templates as structural guides
- Include:
  - Clear "When to use this template" section
  - Inline guidance comments
  - Quality checklist at bottom
  - Distinctions from other templates
- Get approval from @Inversity before merging
- Document in this section after approval

**Universal Template Compliance** (applies to ALL documentation, whether templated or not):
- [ ] Paragraphs under 3 sentences
- [ ] No unexplained jargon
- [ ] "Why" explained for non-obvious steps
- [ ] Exact button/screen labels used
- [ ] Success criteria specific and testable
- [ ] Reading level: 6th grade or lower
- [ ] Validation checkpoints after major steps
- [ ] Inline troubleshooting (not separate section)
- [ ] Clear support escalation path

---

### Markdown Formatting Standards

**Visual Indicators (use consistently):**
- ✅ Success/Validation: "You should see X"
- ⚠️ Warning/Caution: Common mistakes, destructive actions
- 💡 Tip/Best Practice: Optional optimizations

**Structure:**
- `#` for document title only
- `##` for major sections
- `###` for subsections
- Numbered lists for sequential steps
- Bullet lists for non-sequential information
- Code blocks for technical details

**Example Step Format:**
```markdown
### Step 1: Power On Tablet

1. **Plug in** the tablet using the provided charger
2. **Press and hold** the power button for 2-3 seconds
3. **Wait** for the tablet to boot (30-60 seconds)

✅ **You should see:** Android home screen or lock screen

⚠️ **If tablet doesn't power on:**
- Verify charger is plugged into working outlet
- Try different power outlet
- Contact support if no response after 10 seconds
```

---

### Image Guidelines

**Storage Locations:**
- Onboarding screenshots → `assets/images/onboarding/`
- Troubleshooting screenshots → `assets/images/troubleshooting/`
- Feature reference UI → `assets/images/reference/`
- Architecture diagrams → `assets/diagrams/`

**Naming Convention:**
- Be descriptive: `portal-menu-setup-screen.png`
- Include context: `printer-bluetooth-settings-android.png`
- Use hyphens, lowercase

**Technical Requirements:**
- Keep under 1MB (compress if needed)
- Use relative paths: `![Description](../assets/images/section/filename.png)`
- Include alt text for accessibility

---

## Content Requirements by Document Type

### Setup/Onboarding Guides (`onboarding/`)

**Required Sections:**
1. **What's in the Box** - Inventory checklist
2. **Before You Start** - Prerequisites with validation
3. **Step-by-Step Instructions** - Numbered, single-action steps
4. **Verification** - Success criteria checklist
5. **Troubleshooting** - Inline after relevant steps
6. **Support** - Escalation decision tree
7. **Daily Operations** - Opening/closing checklist

**Required Elements:**
- Time estimate for completion
- Validation checkpoints after major steps
- "Why" explanations for non-obvious steps
- Clear escalation paths

---

### Reference Documentation (`reference/`)

**Required Sections:**
1. **Purpose Statement** - What this doc covers
2. **Navigation Overview** - How to access features
3. **Feature-by-Feature Breakdown** - Organized by screen/function
4. **Use Cases** - When to use each feature
5. **Common Issues** - Known limitations

**Avoid:**
- Don't duplicate setup procedures (link to `onboarding/`)
- Don't include detailed troubleshooting (link to `troubleshooting/`)

---

### Troubleshooting Guides (`troubleshooting/`)

**Required Structure:**
1. **Symptom** - What user sees/experiences
2. **Likely Causes** - Ordered by probability
3. **Quick Fixes** - Try these first (under 2 minutes each)
4. **Detailed Fixes** - If quick fixes fail
5. **Escalation** - When to contact support

**Required Elements:**
- Diagnostic steps before fixes
- "What to have ready" for support
- Links to related documentation

---

### Operational Procedures (`operational/`)

**Required Structure:**
1. **When to Use** - Situational context
2. **Prerequisites** - What must be true first
3. **Step-by-Step Procedure** - Numbered actions
4. **Verification** - How to confirm success
5. **Common Issues** - Expected problems

**Audience:** Daily venue operations (not one-time setup)

---

### Internal Documentation (`internal/`)

**Audience:** BlazeBite team only (may contain sensitive info)

**Required Sections:**
1. **Purpose** - What this procedure accomplishes
2. **When to Use** - Triggers for this procedure
3. **Prerequisites** - Access/permissions needed
4. **Detailed Steps** - More technical detail allowed
5. **Verification** - Success criteria
6. **Escalation** - When to involve engineering/leadership

**Note:** Can assume higher technical knowledge than venue-facing docs

---

## Model-Specific Documentation

**When writing with AI assistance, reference:**

- `model-guides/gpt5-documentation-guide.md` - For structured output (tables, schemas)
- `model-guides/gemini-documentation-guide.md` - For large doc analysis (1M token context)
- `model-guides/grok-documentation-guide.md` - For rapid iteration/refinement

**Primary model:** Claude 4.5 Sonnet (85% of documentation generation)

---

## Quality Gates (Before Publishing)

**All documentation must pass:**

### Structure Check
- [ ] Follows approved template from `templates/`
- [ ] Placed in correct directory
- [ ] Steps numbered and sequential
- [ ] Validation checkpoints present
- [ ] Troubleshooting inline or linked
- [ ] Support escalation clear

### Content Quality
- [ ] Paragraphs under 3 sentences
- [ ] No unexplained jargon
- [ ] "Why" explained for non-obvious steps
- [ ] Exact button/screen labels
- [ ] Success criteria testable
- [ ] Reading level appropriate

### Completeness
- [ ] User can complete without external help
- [ ] Common failures addressed
- [ ] Support contact info provided
- [ ] What to have ready for support listed
- [ ] Related docs linked appropriately

### Red Flags (Must Fix)
- ❌ User must "figure out" any step
- ❌ Assumes knowledge not taught earlier
- ❌ Missing validation checks
- ❌ Paragraphs over 3 sentences
- ❌ Vague troubleshooting ("try again")

---

## Testing Documentation

**Before finalizing:**
1. Follow the guide yourself end-to-end
2. Have someone unfamiliar with the process test it
3. Verify all internal links work (especially cross-folder links)
4. Check images display correctly
5. Confirm markdown renders properly
6. Validate against template checklist

---

## Contributing Workflow

1. **Create descriptive branch:** `docs/updating-tablet-setup`
2. **Reference template:** Copy from `templates/` directory
3. **Place in correct folder:** Use structure above
4. **Follow style guidelines:** Max 3 sentences per paragraph
5. **Test on actual devices:** When applicable
6. **Run quality checks:** Use template compliance checklist
7. **Request review:** Tag @Inversity (Joe Wayne)

---

## Key Repository Files

**Templates (always use these):**
- `templates/TEMPLATE_ONBOARDING.md` - All setup/onboarding guides
- `templates/TEMPLATE_TROUBLESHOOTING.md` - Problem resolution docs
- `templates/TEMPLATE_FEATURE_REFERENCE.md` - Feature documentation

**Model Guides (reference when using AI):**
- `model-guides/gpt5-documentation-guide.md` - GPT-5 optimization
- `model-guides/gemini-documentation-guide.md` - Gemini 2.5 Pro strategies
- `model-guides/grok-documentation-guide.md` - Grok Code Fast 1 workflows

**System Architecture:**
- `blazebite-architecture-overview.md` - Complete system overview, data flows, integration points

**Example Documentation:**
- `onboarding/ONBOARDING_TABLET.md` - Primary setup guide example
- `reference/KITCHEN_APP_REFERENCE.md` - Feature documentation example

---

## Support & Contact

**Documentation Maintainer:**
- Joe Wayne (@Inversity)
- For questions about templates, structure, or standards

**Team (for technical clarification):**
- Evan (@devandanger) - Portal/backend questions
- Jeff - Sales/support workflow
- Shawn - App features/business logic

**Venue Support (for documentation context):**
- Mark: 440-231-5818
- Joe: 724-996-6636
- Email: support@blazebite.com

---

## Important Notes

- This is a documentation-only repository (no code or build processes)
- All docs must work offline (venues may have spotty network)
- Focus on clarity over technical sophistication
- Venues are small businesses with minimal IT support
- Documentation = critical operational tool, not nice-to-have
- Internal docs (`internal/`) may contain sensitive information - do not share publicly

---

## Cross-Referencing Guidelines

**When linking between docs:**
- Use relative paths: `[Link text](../onboarding/ONBOARDING_TABLET.md)`
- Link to specific sections: `[Setup Steps](../onboarding/ONBOARDING_TABLET.md#step-by-step-setup-instructions)`
- Reference troubleshooting: "See [Printer Troubleshooting](../troubleshooting/PRINTER_TROUBLESHOOTING.md) for detailed fixes"
- Link templates in PR descriptions: "Created using [TEMPLATE_ONBOARDING.md](../templates/TEMPLATE_ONBOARDING.md)"

**Cross-folder linking examples:**
- From `onboarding/` to `troubleshooting/`: `../troubleshooting/PRINTER_TROUBLESHOOTING.md`
- From `troubleshooting/` to `reference/`: `../reference/KITCHEN_APP_REFERENCE.md`
- From any folder to root: `../blazebite-architecture-overview.md`

---

**Source of Truth:** GitHub Copilot Space "BlazeBite Documentation" contains complete instructions and reasoning behind these standards. All documentation follows patterns defined in that Space.

**Last Updated:** 2025-11-05
**Version:** 1.0
