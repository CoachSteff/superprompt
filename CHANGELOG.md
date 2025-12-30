# Changelog

All notable changes to the SuperPrompt Framework project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- N/A

### Changed
- N/A

### Deprecated
- N/A

### Removed
- N/A

### Fixed
- N/A

### Security
- N/A

## [1.2.1] - 2025-12-30

### Fixed
- 🐛 **Repository Configuration**: Removed `docs/` from `.gitignore` - documentation files are part of the public framework and should be tracked in git
- 📖 **Documentation**: Added missing `craft-attribution.md` to repository with historical attribution for CRAFT framework variants

### Technical Details
- **Version**: 1.2.1 (Patch release - bug fixes only)
- **Breaking Changes**: None
- **Files Modified**: 2 files (.gitignore, docs/craft-attribution.md added)
- **Impact**: New documentation files in `docs/` will now be tracked automatically without requiring `git add -f`
- **Version Naming**: SuperPrompt Framework follows semantic versioning (v1.x.x for repository releases). CRAFTER framework specification remains at v0.2 (technical structure version).

## [1.2.0] - 2025-12-30

### Added
- 🚀 **New Examples for Professional Use Cases**:
  - `blog-writing.md` - Professional blog post creation with critique-revise loop (3 complete examples: how-to guide, thought leadership, case study analysis)
  - `deep-research.md` - Comprehensive evidence-based research analysis (technology evaluation example with source analysis, contradictions, gaps, and recommendations)
  - `image-generation.md` - AI image generation prompting with structured breakdowns (3 visual scenarios: product photography, social media graphic, presentation illustration)
  - `keyword-research.md` - SEO and content strategy keyword research (converted from template with 2 complete examples)
- 🛠️ **Generic Template**: Added `templates/generic-template.md` - fully customizable superprompt template with inline instructions for both human and AI use
- 📖 **Attribution Documentation**: Added `docs/craft-attribution.md` - historical attribution for CRAFT framework variants (Alexander F. Young, Sogeti Labs, Kaleb, Monica Poling, Geeky Gadgets)
- 🎯 **Enhanced Repository**: Updated all examples to CRAFTER v0.2 compliance with professional, cross-domain focus

### Changed
- 📝 **Framework Evolution**: All examples now target any professional (not just coaches/thought leaders) - expanded to serve content creators, researchers, marketers, designers, and technical professionals
- 🔄 **Simplified deep-research.md**: Reduced from 3 examples to 1 comprehensive technology evaluation example for better clarity and usability
- 📚 **Documentation Reorganization**: 
  - `examples/README.md` - New categorization (Coaching & Leadership, Research & Analysis, Content Creation & Marketing, Documentation & Technical Writing, Meta Examples)
  - `PROMPTS.md` - Updated index with 7 core examples plus 2 meta examples
  - `README.md` - Updated examples table to reflect current repository state (8 examples total)
  - `GETTING_STARTED.md` - Updated all example lists and reorganized by use case
  - `AGENTS.md` - Updated directory structure to show current files
- 🏷️ **Version Updates**: All framework references updated from v0.1 to v0.2

### Removed
- ❌ **Streamlined Examples**: Deleted `podcast-generation.md`, `team-retrospective.md`, `opportunity-scan.md` to maintain focused, high-quality example set

### Technical Details
- **Version**: 1.2.0 (Minor release - new features, backward compatible)
- **Breaking Changes**: None
- **Examples Count**: 9 total (7 domain-specific examples + 2 meta examples for creating superprompts)
- **Templates Count**: 2 (generic-template.md for any use case, keyword-researcher.md for SEO)
- **Framework Compliance**: 100% CRAFTER v0.2 specification compliance
- **Files Modified**: 18 files updated, 6 files created, 3 files removed
- **Cross-Domain Applicability**: Examples now serve professionals across all industries and roles

### Migration Guide
No migration required. All changes are additive and maintain full backward compatibility. Users of v1.1.0 can:
- Continue using existing examples (coaching-reflection, documentation-cleanup, research-synthesis remain unchanged in structure)
- Adopt new examples for additional use cases (blog writing, research, image generation, keyword research)
- Use the new generic template to create custom superprompts for any scenario
- Reference craft-attribution.md for historical context on CRAFT framework variants

### Notes for Contributors
- All new examples follow professional, cross-domain focus (not coaching-specific)
- Examples should be production-ready with 2-3 complete input/output demonstrations
- Use CRAFTER v0.2 structure: Context → Role → Action → Format → Target & Tone → Examples → Refining
- Attribution footer required: `Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)`

## [1.1.0] - 2025-10-29

### Added
- Initial framework enhancements and improvements

### Changed
- Framework refinements and documentation updates

## [1.0.0] - 2025-10-20

### Added
- 🚀 **Initial Release**: SuperPrompt Framework v1.0.0
- 📚 **Core Framework**: Basic prompt engineering framework structure
- 🔧 **Context Management**: Initial context engineering capabilities
- 📖 **Documentation**: Comprehensive README and contributing guidelines
- 🛡️ **Security**: Security policy and vulnerability reporting process
- 🤝 **Community**: Code of conduct and contribution guidelines
- 📝 **Research**: Initial research on context engineering and AI-powered second brain
- 🏗️ **Infrastructure**: GitHub repository setup with proper exclusions
- 📦 **Package**: NPM package configuration for distribution
- 🔒 **License**: MIT license for open source distribution

### Technical Details
- **Repository**: [https://github.com/CoachSteff/superprompt](https://github.com/CoachSteff/superprompt)
- **Author**: Steff VanHaverbeke ([@CoachSteff](https://github.com/CoachSteff))
- **License**: MIT
- **Node.js**: >=14.0.0
- **Keywords**: ai, prompt-engineering, context-management, framework, artificial-intelligence, llm, prompt-optimization, ai-tools

### Files Included
- `README.md` - Project overview and documentation
- `package.json` - NPM package configuration
- `LICENSE` - MIT license
- `CONTRIBUTING.md` - Contribution guidelines
- `CODE_OF_CONDUCT.md` - Community code of conduct
- `SECURITY.md` - Security policy and vulnerability reporting
- `CHANGELOG.md` - This changelog
- `.gitignore` - Git ignore configuration
- `meta.md` - Project metadata (archived)
- `schema.jsonld` - JSON-LD schema definition
- `research/` - Research documentation and findings

### Excluded from Release
- `.claude/` - AI Claude directory
- `.cursor/` - Cursor IDE directory
- `.cursorrules` - Cursor rules file
- `docs/` - Documentation directory (development docs)

### Research Foundation
This release builds upon research into "The Convergence of Context Engineering and the AI-Powered Second Brain," establishing a framework for advanced prompt engineering and context management in AI applications.

---

## Release Notes Format

### Version Numbering
- **MAJOR** (X.0.0): Breaking changes, incompatible API changes
- **MINOR** (X.Y.0): New features, backward-compatible additions  
- **PATCH** (X.Y.Z): Bug fixes, backward-compatible fixes

### Change Categories
- **Added**: New features
- **Changed**: Changes to existing functionality
- **Deprecated**: Soon-to-be removed features
- **Removed**: Removed features
- **Fixed**: Bug fixes
- **Security**: Security improvements

### Links
- [Keep a Changelog](https://keepachangelog.com/)
- [Semantic Versioning](https://semver.org/)
- [SuperPrompt Framework](https://github.com/CoachSteff/superprompt)
