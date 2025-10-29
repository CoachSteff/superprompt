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

## [1.1.0] - 2025-10-29

### Added
- 🚀 **CRAFTER v0.2 Compliance**: All examples and templates now follow the updated CRAFTER v0.2 specification
- 📚 **Enhanced Examples**: Updated 6 examples with improved structure and content
  - `coaching-reflection.md` - Enhanced with comprehensive context and action steps
  - `team-retrospective.md` - Improved role definitions and format specifications
  - `opportunity-scan.md` - Added detailed reasoning policy and self-check criteria
  - `documentation-cleanup.md` - Enhanced with specific expertise areas and constraints
  - `research-synthesis.md` - Improved with comprehensive action steps and examples
  - `example-mode-b-creation.md` - Updated to CRAFTER v0.2 structure
- 🛠️ **Template Improvements**: Updated `keyword-researcher.md` template with CRAFTER v0.2 structure
- 📖 **Documentation**: Added comprehensive `examples/README.md` with usage guidance
- 🎯 **Target & Tone Integration**: Converted T component from "Target Audience" to integrated "Target & Tone"

### Changed
- 🔄 **CRAFTER Structure**: Updated all examples to use proper CRAFTER v0.2 headers
  - Context sections now include common scenarios and constraints
  - Role definitions enhanced with specific expertise areas
  - Action steps made more comprehensive and actionable
  - Format sections standardized with clear output structure
  - Target & Tone sections provide integrated audience and tone guidance
  - Examples sections include practical input/output demonstrations
  - Refining sections added for iteration guidance
- 📝 **Attribution Updates**: All examples now use "CRAFTER (SuperPrompt Framework v0.2)" attribution
- 🏗️ **Template Structure**: Templates now follow CRAFTER v0.2 specification with placeholders

### Technical Details
- **Version**: 1.1.0 (Minor release - new features, backward compatible)
- **Breaking Changes**: None
- **Compatibility**: Full backward compatibility maintained
- **Files Updated**: 7 files modified, 1 new file added
- **Framework Compliance**: 100% CRAFTER v0.2 specification compliance

### Migration Guide
No migration required. All changes are additive and maintain full backward compatibility. Existing users can continue using the framework as before, with access to enhanced examples and templates.

## [1.0.0] - 2025-01-20

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
