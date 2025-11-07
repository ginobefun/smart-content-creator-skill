# Changelog

All notable changes to the Smart Content Creator skill will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2025-11-07

### Added
- **New Reference Guide**: `writing_principles.md` - First principles approach to writing quality
  - Core formula: Writing Quality = Information Transfer × Emotional Resonance × Cognitive Comfort
  - Cognitive load management techniques
  - Reward density strategies
  - Theoretical foundation for all writing techniques

### Changed
- **Skill Metadata Optimization**:
  - Unified skill name from `content-synthesizer` to `smart-content-creator`
  - Simplified description from ~460 characters to ~200 characters for better Claude comprehension

- **Enhanced Skill Structure**:
  - Added explicit `Activation Triggers` section at the beginning
  - Added `Reference Loading Strategy` section with clear priority hierarchy
  - Marked 4 core guides with ⭐ (writing_principles, personal_voice, depth, natural_language)

- **Streamlined Workflow**:
  - Reduced SKILL.md from 737 lines to 401 lines (45.6% reduction)
  - Removed "Creative Faucet Principle" section (moved to optional context)
  - Simplified step-by-step instructions while preserving all core functionality
  - Reorganized content for better clarity and faster comprehension

- **Documentation Updates**:
  - Updated CLAUDE.md to reflect 11 reference guides (was 10)
  - Updated skill package size documentation (~82KB, was ~60KB)

### Improved
- **Reference Guides Enhancement**:
  - Expanded `blog_guide.md` with additional examples and techniques
  - Enhanced `depth_guide.md` with more depth analysis methods
  - Significantly expanded `natural_language.md` with comprehensive anti-AI patterns
  - Major expansion of `xiaohongshu_guide.md` with cultural localization details

### Technical
- Skill package size: 78KB (optimized from previous 82KB)
- Total reference guides: 11 comprehensive documents
- SKILL.md: 401 lines (streamlined from 737 lines)

## [1.0.0] - 2025-11-06

### Added
- Initial release of Smart Content Creator skill
- 6 core content formats:
  - Text: Blog Posts, Xiaohongshu Notes, Twitter Long-Form
  - Visual: Mind Maps, Infographics, Charts & Diagrams
- 10 comprehensive reference guides:
  - `personal_voice_guide.md` - Voice identification and preservation
  - `depth_guide.md` - Deep content creation methodology
  - `natural_language.md` - Anti-AI writing patterns
  - `writing_styles.md` - Flexible style frameworks
  - `blog_guide.md` - Blog post creation principles
  - `xiaohongshu_guide.md` - Chinese social media content
  - `twitter_article_guide.md` - Twitter long-form articles
  - `mindmap_guide.md` - Mind mapping techniques
  - `infographic_guide.md` - Information design principles
  - `visualization_guide.md` - Charts and diagrams guide
- Core capabilities:
  - Personal voice preservation system
  - Deep content creation methodology
  - Natural language anti-AI patterns
  - Cultural localization (English/Chinese)
  - Flexible style frameworks
  - Smart visualization selection
- Complete workflow from input gathering to content delivery
- Quality standards and error prevention guidelines
- Cross-skill collaboration support

[1.1.0]: https://github.com/yourusername/smart-content-creator-skill/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/yourusername/smart-content-creator-skill/releases/tag/v1.0.0
