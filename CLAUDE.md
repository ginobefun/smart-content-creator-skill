# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Smart Content Creator** is a Claude AI skill (.skill file) that transforms reading materials and personal insights into polished, shareable content. It emphasizes natural, human-like expression while avoiding AI-style writing patterns.

### Core Purpose

This skill helps users create authentic content in **6 core formats + advanced visualizations**:

**Text Formats**:
- Blog Posts (2000-4000 words) - Long-form engaging content
- Xiaohongshu Notes (800-1500 chars) - Authentic Chinese social media content
- Twitter Long-Form (1000-4000 words) - Professional X platform articles

**Visual Formats**:
- Mind Maps - Hierarchical knowledge organization
- Infographics - Data-driven storytelling with visual impact
- Charts & Diagrams - Flowcharts, concept maps, timelines, and more

**Key Capabilities**:
- Deep Content Creation - Multi-layered thinking and counter-intuitive insights
- Personal Voice Preservation - Capture and maintain authentic writing style
- Natural Expression - Content that reads like human writing
- Cultural Localization - Properly adapted for English/Chinese
- Anti-AI Patterns - Comprehensive guidelines to avoid robotic writing

## Repository Structure

### Source Files

- **`src/smart-content-creator/`** - Source files for the skill (tracked in Git)
  - `SKILL.md` - Main workflow and content creation process
  - `references/` - Detailed format guides (11 total)
    - `writing_principles.md` ⭐ - First principles approach to writing quality
    - `personal_voice_guide.md` ⭐ - Voice identification and preservation
    - `depth_guide.md` ⭐ - Deep content creation methodology
    - `natural_language.md` ⭐ - Critical anti-AI writing guide
    - `writing_styles.md` - Flexible style frameworks
    - `blog_guide.md` - Blog post creation principles
    - `xiaohongshu_guide.md` - Chinese social media content
    - `twitter_article_guide.md` - Twitter long-form articles
    - `mindmap_guide.md` - Mind mapping techniques
    - `infographic_guide.md` - Information design principles
    - `visualization_guide.md` - Charts and diagrams guide

### Built Package

- **`smart-content-creator.skill`** - The packaged skill file (built from `src/`)
  - Format: Standard Claude skill package (ZIP archive)
  - Size: ~82KB (optimized for context window efficiency)
  - Built using: `./build.sh`

### Build Script

- **`build.sh`** - Bash script to package source files into `.skill` file
  - Copies files from `src/smart-content-creator/`
  - Creates ZIP archive with proper structure
  - Shows size and contents summary

### Documentation Files

- **`README.md`** - Main documentation with comprehensive usage guide (English)
- **`README_CN.md`** - Complete Chinese documentation
- **`CONTRIBUTING.md`** - Contribution guidelines and skill development rules
- **`CHANGELOG.md`** - Version history
- **`LICENSE`** - MIT License

## Development Workflow

### Editing the Skill

**Standard workflow:**

```bash
# 1. Edit source files directly
vim src/smart-content-creator/SKILL.md
vim src/smart-content-creator/references/natural_language.md

# 2. Rebuild the skill package
./build.sh

# 3. Test by importing the .skill file into Claude

# 4. Commit both source and built files
git add src/ smart-content-creator.skill
git commit -m "feat: enhance natural language guidelines"
```

**Examining the packaged skill:**

```bash
# List contents of the skill archive
unzip -l smart-content-creator.skill

# View specific file without extracting
unzip -p smart-content-creator.skill smart-content-creator/SKILL.md
```

### Key Architectural Decisions

1. **Personal Voice First**: The skill prioritizes understanding and preserving the user's authentic voice before generating any content.

2. **Anti-AI Pattern Library**: Comprehensive guidelines to avoid common AI writing patterns:
   - Excessive transitional phrases
   - Overuse of quotation marks
   - Buzzword overload
   - Formulaic structures
   - Generic advice

3. **Flexible Style Frameworks**: Instead of rigid templates, provides adaptable style approaches:
   - Thoughtful Explorer
   - Practical Guide
   - Analytical Observer
   - Storytelling Teacher
   - Conversational Expert

4. **Cultural Localization**: Special handling for Chinese content to ensure authentic expressions without translation artifacts.

5. **Multi-Format Support**: Single workflow that adapts to different content types and platforms.

## Skill Trigger Conditions

The skill auto-triggers when users:

- Say: "create a blog post", "write Xiaohongshu content", "make a mind map", "turn this into..."
- Request content transformation or visualization
- Ask for platform-specific content (Twitter, blog, social media)
- Request diagrams, charts, or infographics

## Adding New Features

### Adding a New Content Format

1. Create `src/smart-content-creator/references/new_format_guide.md` following this structure:
   - Overview: What is this format?
   - Platform characteristics
   - Audience expectations
   - Content structure guidelines
   - Examples and anti-patterns
   - Cultural considerations (if applicable)

2. Reference it in `src/smart-content-creator/SKILL.md` in the format selection section

3. Update `README.md` features section

4. Rebuild: `./build.sh`

5. Test the new skill package in Claude

### Adding New Writing Styles

1. Add to `src/smart-content-creator/references/writing_styles.md`
2. Include: style characteristics, when to use, voice patterns, examples
3. Ensure it's flexible, not a rigid template
4. Rebuild: `./build.sh`

### Adding New Visualization Types

1. Update `src/smart-content-creator/references/visualization_guide.md`
2. Include: when to use, structure guidelines, Mermaid examples
3. Add to README visualization types section
4. Rebuild: `./build.sh`

### Modifying the Workflow

- Core workflow is in `src/smart-content-creator/SKILL.md`
- Key sections:
  - Voice discovery process
  - Depth assessment
  - Content generation workflow
  - Quality standards
- After changes, run `./build.sh` to rebuild the package

## Testing Changes

Before committing skill modifications:

1. Edit files in `src/smart-content-creator/`
2. Rebuild: `./build.sh`
3. Import `smart-content-creator.skill` into Claude (Desktop or Web)
4. Test with various scenarios:
   - Different content formats (blog, Xiaohongshu, Twitter)
   - Different writing styles
   - Visualization requests
   - Voice preservation accuracy
   - Natural language quality (no AI patterns)
5. Verify all reference documents load correctly
6. Check existing functionality still works
7. Commit both source and built files

## Important Conventions

### Writing Style for Skill Content

- **Natural over formal** - Content should sound human, not robotic
- **Specific examples** - Concrete over abstract explanations
- **Cultural awareness** - Properly localized expressions
- **Action-oriented** - Always provide practical guidance
- **Flexibility over rigidity** - Frameworks not templates

### Commit Message Format

- `feat:` - New feature or content format
- `fix:` - Bug fix in workflow or references
- `docs:` - Documentation changes
- `refactor:` - Restructuring without behavior change
- `enhance:` - Improvements to existing features

### File Encoding and Format

- All markdown files use UTF-8 encoding
- Line endings: LF (Unix-style)
- Max line length: No hard limit (markdown flows naturally)
- Skill archive: Standard ZIP format

## Common Tasks

**Edit skill workflow:**

```bash
# Edit the main workflow
vim src/smart-content-creator/SKILL.md

# Or view it directly
cat src/smart-content-creator/SKILL.md | less
```

**Edit content guides:**

```bash
# Edit a specific guide
vim src/smart-content-creator/references/natural_language.md

# View all guides
ls -lh src/smart-content-creator/references/
```

**Build and test:**

```bash
# Build the skill package
./build.sh

# Check built file size
ls -lh smart-content-creator.skill

# Validate structure
unzip -t smart-content-creator.skill

# View packaged contents
unzip -l smart-content-creator.skill
```

**Quick comparison:**

```bash
# Compare source vs packaged version
diff <(cat src/smart-content-creator/SKILL.md) \
     <(unzip -p smart-content-creator.skill smart-content-creator/SKILL.md)
```

## Quality Standards

When modifying the skill, ensure:

- ✅ Content sounds natural and human-like
- ✅ Personal voice is preserved
- ✅ No AI writing patterns (excessive transitions, buzzwords, etc.)
- ✅ Cultural localization is appropriate
- ✅ Examples are concrete and actionable
- ✅ Total size remains under 100KB for context efficiency

Avoid:

- ❌ Rigid templates that constrain creativity
- ❌ Generic, one-size-fits-all advice
- ❌ Translation-style language (especially for Chinese)
- ❌ AI-typical phrases and structures
- ❌ Overlooking personal voice in favor of format

## Version Information

- **Current version: 1.0.0**
- **What's new in 1.0:**
  - 6 core content formats (3 text + 3 visual)
  - 11 comprehensive reference guides
  - Writing principles: First principles approach to writing quality
  - Personal voice preservation system
  - Deep content creation methodology
  - Natural language anti-AI patterns
  - Cultural localization (English/Chinese)
  - Flexible style frameworks
  - Smart visualization selection
- Initial release: 2025-11-06
- Compatible with: Claude Sonnet 4.5+
- License: MIT

## Integration with Other Skills

### With Deep Reading Analyst

This skill is designed to complement Deep Reading Analyst:

1. Use Deep Reading Analyst to analyze source material
2. Use Smart Content Creator to transform insights into shareable content
3. Result: Deep understanding → polished, authentic output

### Content Creation Workflow

```
Reading Material
    ↓
[Deep Reading Analyst] - Analysis & Understanding
    ↓
Personal Insights + Analysis Results
    ↓
[Smart Content Creator] - Content Generation
    ↓
Polished Content (Text + Visualizations)
```

## Key Differentiators

What makes this skill unique:

1. **Voice Preservation**: Actively discovers and maintains user's authentic voice
2. **Depth Focus**: Multi-layered thinking for substantive content
3. **Anti-AI Engineering**: Comprehensive safeguards against robotic writing
4. **Cultural Intelligence**: True localization, not just translation
5. **Flexible Frameworks**: Adaptable styles, not rigid templates
6. **Integrated Visuals**: Text and visualization in unified workflow

## Philosophy

**The goal isn't to hide that AI helped. The goal is to create content so natural, so authentic, so valuable that nobody cares whether AI was involved.**

**Great content is great content.**

