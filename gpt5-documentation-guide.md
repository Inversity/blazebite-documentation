# GPT-5 Documentation Optimization Guide

**Model-Specific Guide for BlazeBite Documentation Space**

This guide covers when and how to use GPT-5 effectively within the BlazeBite Documentation Space's multi-model workflow (5% non-Claude usage).

---

## 🎯 When to Use GPT-5 Over Claude

GPT-5 excels in specific scenarios where Claude may struggle or be less efficient:

### ✅ Ideal Use Cases

1. **Structured Output Generation**
   - Complex JSON schemas
   - API response formats
   - Database schema definitions
   - Configuration file generation

2. **Table and Matrix Creation**
   - Feature comparison tables
   - Multi-dimensional matrices
   - Data transformation tables
   - Technical specification grids

3. **API Documentation**
   - Endpoint reference documentation
   - Request/response examples
   - Parameter specification tables
   - Error code documentation

4. **Technical Specifications**
   - Hardware specification sheets
   - Protocol documentation
   - Integration specification documents
   - Technical requirement matrices

### ❌ When NOT to Use GPT-5

- Long-form narrative documentation (use Claude 3.5 Sonnet)
- Creative user-facing content (use Claude 3.5 Sonnet)
- General documentation editing (use Claude 3.5 Sonnet)
- Content requiring nuanced tone (use Claude 3.5 Sonnet)

---

## ⚙️ Reasoning_Effort Parameter Configuration

GPT-5 includes a `reasoning_effort` parameter that controls computation time vs. quality tradeoffs.

### Configuration Guidelines

```python
# Low effort (fast, simple tasks)
reasoning_effort = "low"
# Use for: Simple table generation, basic formatting

# Medium effort (balanced)
reasoning_effort = "medium"  # DEFAULT
# Use for: Standard API docs, moderate complexity tables

# High effort (complex tasks)
reasoning_effort = "high"
# Use for: Complex schema validation, multi-dimensional matrices
```

### Effort Level Decision Matrix

| Task Complexity | Structured Output | Time Sensitivity | Recommended Effort |
|-----------------|-------------------|------------------|-------------------|
| Simple | Basic JSON | High | Low |
| Moderate | API schemas | Medium | Medium |
| Complex | Multi-layer schemas | Low | High |
| Very Complex | Nested matrices | Low | High |

**Best Practice:** Start with `medium` and adjust based on output quality.

---

## 🛑 Explicit Stopping Rules Requirements

GPT-5 requires explicit stopping instructions to prevent over-generation.

### Required Stopping Patterns

Always include explicit stopping rules in your prompts:

```markdown
# ✅ GOOD: Explicit stopping rule
Create API documentation for the /orders endpoint.
Stop after completing the example response section.

# ❌ BAD: No stopping rule
Create API documentation for the /orders endpoint.
```

### Stopping Rule Templates

**For Tables:**
```
Generate a feature comparison table.
Stop after completing the table with all 5 features listed.
Do not add additional commentary after the table.
```

**For API Docs:**
```
Document the authentication endpoints.
Stop after completing:
1. Endpoint description
2. Parameters table
3. Example request
4. Example response
Do not generate additional endpoints.
```

**For Specifications:**
```
Create hardware specifications for the tablet.
Stop after completing the specifications table.
Do not add setup instructions or usage notes.
```

---

## 📊 Structured Output Patterns for Tables/Matrices

GPT-5 excels at generating structured tabular data when properly prompted.

### Simple Comparison Table Pattern

```markdown
Prompt template:
---
Create a comparison table for [ITEMS] with the following columns:
- Column 1: [NAME]
- Column 2: [NAME]
- Column 3: [NAME]

Include exactly [N] rows.
Format as markdown table.
Stop after completing the table.
---
```

**Example:**
```markdown
Create a comparison table for BlazeBite device types with the following columns:
- Device Type
- Screen Size
- Primary Use
- Setup Time

Include exactly 3 rows (Kitchen Tablet, Kiosk, Portal).
Format as markdown table.
Stop after completing the table.
```

**Output:**
```markdown
| Device Type | Screen Size | Primary Use | Setup Time |
|-------------|-------------|-------------|------------|
| Kitchen Tablet | 10-12 inches | Order management | 15-20 min |
| Kiosk | 15-17 inches | Customer ordering | 25-30 min |
| Portal | Desktop/Mobile | Admin & reporting | 5-10 min |
```

### Multi-Dimensional Matrix Pattern

```markdown
Prompt template:
---
Create a matrix showing [RELATIONSHIP] between [ENTITY_A] and [ENTITY_B].

Rows: [LIST_ROWS]
Columns: [LIST_COLUMNS]

Cell values should indicate [CRITERIA].
Format as markdown table with clear headers.
Stop after completing the matrix.
---
```

**Example:**
```markdown
Create a matrix showing compatibility between printer models and connection types.

Rows: TSP100, TSP143, TM-T20
Columns: Bluetooth, USB, Ethernet, WiFi

Cell values should indicate: ✅ Supported, ⚠️ Limited, ❌ Not Supported
Format as markdown table with clear headers.
Stop after completing the matrix.
```

### Nested Data Structure Pattern

```markdown
Prompt template:
---
Generate a [FORMAT] structure for [PURPOSE] with the following schema:
```json
{
  "parent_field": {
    "nested_field_1": "type",
    "nested_field_2": "type"
  }
}
```

Include example values.
Validate against the schema.
Stop after generating the complete structure.
---
```

---

## 💡 Prompting Patterns for Technical Specifications

### Pattern 1: API Endpoint Documentation

```markdown
Document the [ENDPOINT_NAME] API endpoint with the following structure:

## Endpoint: [METHOD] [PATH]

**Description:** [1-2 sentences]

**Request Parameters:**
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| [name] | [type] | [yes/no] | [description] |

**Example Request:**
```[language]
[code example]
```

**Response Format:**
```json
[response schema]
```

**Status Codes:**
| Code | Meaning |
|------|---------|
| [code] | [description] |

Stop after completing all sections.
```

### Pattern 2: Hardware Specification Sheet

```markdown
Generate hardware specifications for [DEVICE_NAME] in the following format:

## [DEVICE_NAME] Technical Specifications

**Physical Characteristics:**
| Specification | Value |
|---------------|-------|
| Dimensions | [value] |
| Weight | [value] |
| Screen Size | [value] |

**Performance:**
| Specification | Value |
|---------------|-------|
| Processor | [value] |
| RAM | [value] |
| Storage | [value] |

**Connectivity:**
| Specification | Value |
|---------------|-------|
| WiFi | [value] |
| Bluetooth | [value] |
| Ports | [value] |

Stop after completing all specification tables.
```

### Pattern 3: Configuration Schema Documentation

```markdown
Document the configuration schema for [COMPONENT_NAME]:

## Configuration Schema

**Schema Definition:**
```json
{
  "field_name": {
    "type": "string",
    "required": true,
    "default": "value",
    "description": "Description"
  }
}
```

**Field Reference:**
| Field | Type | Required | Default | Description |
|-------|------|----------|---------|-------------|
| [name] | [type] | [yes/no] | [value] | [description] |

**Example Configuration:**
```json
{
  "example": "complete configuration"
}
```

Stop after completing the example configuration.
```

---

## ⚠️ Limitations and Workarounds

### Known Limitations

1. **Verbosity in Explanations**
   - **Issue:** GPT-5 tends to over-explain technical concepts
   - **Workaround:** Use explicit stopping rules and specify "concise" output

2. **Inconsistent Markdown Formatting**
   - **Issue:** May use varied heading levels or list formats
   - **Workaround:** Specify exact markdown format in prompt (e.g., "Use ### for all section headers")

3. **Over-generation Beyond Scope**
   - **Issue:** Continues generating related but unasked-for content
   - **Workaround:** Use strong stopping rules: "Stop immediately after [specific section]"

4. **Table Alignment Issues**
   - **Issue:** Sometimes creates misaligned markdown tables
   - **Workaround:** Request "properly aligned markdown table" and specify column count

### Workaround Examples

**Problem:** GPT-5 generates extra sections beyond what was requested

```markdown
# ❌ Original prompt:
Create API documentation for /login endpoint.

# ✅ Improved prompt:
Create API documentation for /login endpoint.
Include ONLY:
1. Endpoint description
2. Parameters table
3. Example request
4. Example response
Stop immediately after the example response.
Do not add related endpoints, troubleshooting, or additional notes.
```

**Problem:** Inconsistent table formatting

```markdown
# ❌ Original prompt:
Create a feature comparison table.

# ✅ Improved prompt:
Create a feature comparison table.
Use exactly 4 columns and 5 rows.
Ensure all cells are populated.
Use markdown table format with proper | alignment.
Stop after completing the table.
```

---

## ✅ Best Practices Summary

### Configuration
- ✅ Start with `reasoning_effort="medium"` and adjust based on complexity
- ✅ Use higher effort for nested schemas and complex matrices
- ✅ Use lower effort for simple table generation

### Prompting
- ✅ **Always include explicit stopping rules**
- ✅ Specify exact output format (JSON, markdown table, etc.)
- ✅ Define schema structure before requesting generation
- ✅ Use numbered lists for multi-step requirements
- ✅ Request "concise" output to reduce verbosity

### Quality Control
- ✅ Validate structured output against schema requirements
- ✅ Check table alignment and completeness
- ✅ Verify stopping rules were followed
- ✅ Review for over-generation beyond scope

### When to Switch Models
- ✅ Use **Claude 3.5 Sonnet** for narrative documentation
- ✅ Use **Gemini 2.5 Pro** for large document analysis
- ✅ Use **Grok Code Fast 1** for rapid iteration on variations

### Documentation Workflow Integration

**Typical GPT-5 Workflow in BlazeBite Documentation:**

1. **Claude** generates initial user-facing guide (95% of content)
2. **GPT-5** generates API reference tables (5% structured content)
3. **Claude** integrates and finalizes (final review)

**Example Task Distribution:**
```markdown
Task: Create device setup documentation with API integration

- Claude: Write setup instructions, troubleshooting, user guidance (main content)
- GPT-5: Generate API endpoint reference table (structured data)
- Claude: Integrate API table into setup guide and finalize
```

---

## 🔄 Quick Reference

### Use GPT-5 For:
- ✅ API documentation tables
- ✅ Technical specification sheets
- ✅ Configuration schemas
- ✅ Feature comparison matrices
- ✅ Structured JSON generation

### Always Include:
- ✅ Explicit stopping rules
- ✅ Exact format specification
- ✅ `reasoning_effort` setting
- ✅ Clear scope boundaries

### Avoid GPT-5 For:
- ❌ Long-form guides
- ❌ User-facing instructions
- ❌ Creative content
- ❌ Tone-sensitive writing

---

**Last Updated:** 2025-11-05  
**Model Version:** GPT-5  
**Recommended Usage:** 5% of BlazeBite documentation tasks
