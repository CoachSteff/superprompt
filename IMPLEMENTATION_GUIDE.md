# CRAFTER v0.2 Implementation Guide

**Complete deployment playbook for upgrading from v0.1 to v0.2**

Version: 0.2  
Last Updated: January 2025  
Author: Steff Vanhaverbeke

---

## Overview

This guide walks you through deploying CRAFTER v0.2 to your GitHub repository. It covers:
- File deployment
- Testing procedures
- Backward compatibility
- URL strategy
- Rollout planning

**Time investment:** 2-4 hours for complete deployment and testing

---

## What's New in v0.2

### Major Changes

**1. T Component Merge: Target & Tone**
- **Before (v0.1):** T = Target audience only
- **After (v0.2):** T = Target & Tone (integrated)
- **Rationale:** Audience characteristics naturally determine communication approach
- **Impact:** Reduces confusion, matches real-world practice

**2. Dual-Mode Capability**
- **Mode A:** Meta-prompt enhancement (restructure existing prompts)
- **Mode B:** Superprompt creation (generate new prompts)
- **Benefit:** Single entry point (`ai.md`) handles both use cases

### New Files

| File | Size | Purpose | Location |
|------|------|---------|----------|
| `ai.md` | 15KB | Dual-mode AI briefing | Repository root |
| `01-CRAFTER-SPEC.md` | 20KB | Updated framework spec | `/ai-context/` |
| `example-mode-a-enhancement.md` | 7KB | Enhancement demo | `/examples/` |
| `example-mode-b-creation.md` | 11KB | Creation demo | `/examples/` |
| `IMPLEMENTATION_GUIDE.md` | 13KB | This document | Repository root |
| `QUICK_REFERENCE.md` | 6KB | Cheat sheet | Repository root |

**Total:** 6 files, 72KB

---

## Deployment Phases

### Phase 1: Pre-Deployment (30 minutes)

#### 1.1 Review Files

Before uploading, review each file:

```bash
# If files are in Desktop folder
cd ~/Desktop/superprompt-v0.2

# Review each file
cat ai.md
cat 01-CRAFTER-SPEC.md
cat example-mode-a-enhancement.md
cat example-mode-b-creation.md
cat IMPLEMENTATION_GUIDE.md
cat QUICK_REFERENCE.md
```

**Checklist:**
- [ ] All files present (6 total)
- [ ] No placeholder text (`[TODO]`, `[FILL IN]`)
- [ ] Attribution footer in all examples
- [ ] Version numbers correct (0.2)
- [ ] Links working (relative paths correct)

#### 1.2 Backup Current Repository

```bash
# Clone your current repository
cd ~/Development
git clone https://github.com/CoachSteff/superprompt-framework.git superprompt-backup

# Create backup branch
cd superprompt-framework
git checkout -b backup-v0.1
git push origin backup-v0.1
```

**Why:** Allows rollback if issues arise.

#### 1.3 Create Feature Branch

```bash
cd ~/Development/superprompt-framework
git checkout main
git pull origin main
git checkout -b feat/v0.2-release
```

---

### Phase 2: File Deployment (30 minutes)

#### 2.1 Copy New Files

```bash
# From your Desktop folder to repository
cd ~/Development/superprompt-framework

# Copy ai.md to repository root
cp ~/Desktop/superprompt-v0.2/ai.md ./

# Copy updated spec to ai-context
cp ~/Desktop/superprompt-v0.2/01-CRAFTER-SPEC.md ./ai-context/

# Copy examples to examples folder
cp ~/Desktop/superprompt-v0.2/example-mode-a-enhancement.md ./examples/
cp ~/Desktop/superprompt-v0.2/example-mode-b-creation.md ./examples/

# Copy guides to root
cp ~/Desktop/superprompt-v0.2/IMPLEMENTATION_GUIDE.md ./
cp ~/Desktop/superprompt-v0.2/QUICK_REFERENCE.md ./
```

#### 2.2 Update README.md

Key sections to update:

**Version reference:**
```markdown
Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)
```

**T component definition:**
```markdown
| Component | Purpose | Example |
|-----------|---------|---------|
| T — Target & Tone | WHO uses this + HOW to communicate | "Marketing managers (action-oriented) — Direct, scannable, lead with takeaways" |
```

**Add dual-mode explanation:**
```markdown
## Two Ways to Use CRAFTER

**Mode A: Enhance Existing Prompts**
Have a prompt that needs improvement? CRAFTER can restructure it.
- Example: [mode-a-enhancement.md](./examples/example-mode-a-enhancement.md)

**Mode B: Create New Superprompts**
Building from scratch? CRAFTER provides the framework.
- Example: [mode-b-creation.md](./examples/example-mode-b-creation.md)

**Entry point:** [ai.md](./ai.md) — Single instruction file for AI models
```

#### 2.3 Update PROMPTS.md

Add new examples to the index:

```markdown
| Example | Use Case | Mode | Pattern | Link |
|---------|----------|------|---------|------|
| Meta-Prompt Enhancement | Restructuring vague prompts | Mode A | Enhancement | [View](./examples/example-mode-a-enhancement.md) |
| Difficult Conversation Coach | Workplace communication prep | Mode B | Creation | [View](./examples/example-mode-b-creation.md) |
```

#### 2.4 Stage and Commit

```bash
git add .
git status  # Review what's being committed

# Commit with conventional commit format
git commit -m "feat: Release v0.2 with Target & Tone merge and dual-mode capability

- Merge T component: Target + Tone integration
- Add dual-mode capability (enhancement vs creation)
- Add ai.md as unified entry point
- Update 01-CRAFTER-SPEC.md with v0.2 changes
- Add mode-a and mode-b example demonstrations
- Include implementation guide and quick reference

BREAKING CHANGE: T component now includes Tone (previously Target only)"
```

---

### Phase 3: Testing (1 hour)

#### 3.1 Smoke Test: Mode A (Enhancement)

**Test with Claude:**
```
Read https://github.com/CoachSteff/superprompt-framework/blob/feat/v0.2-release/ai.md

Enhance this prompt:
"You're a data analyst. Look at this sales data and find insights."
```

**Expected behavior:**
- AI detects Mode A
- Restructures using CRAFTER
- Includes all 7 components
- Shows "Changes Made" section

**Success criteria:**
- [ ] Mode detected correctly
- [ ] All 7 components present
- [ ] T component shows Target & Tone integration
- [ ] Output format matches specification

#### 3.2 Smoke Test: Mode B (Creation)

**Test with Claude:**
```
Read https://github.com/CoachSteff/superprompt-framework/blob/feat/v0.2-release/ai.md

Create a superprompt for writing better email subject lines for marketing campaigns.
```

**Expected behavior:**
- AI detects Mode B
- Generates complete superprompt
- Uses proper CRAFTER structure
- Includes examples and refining guidance

**Success criteria:**
- [ ] Mode detected correctly
- [ ] All 7 components present
- [ ] T component formatted as: Target + Tone
- [ ] Attribution footer included
- [ ] Self-test checklist shows 7/7

#### 3.3 Cross-Model Testing

Test with multiple AI models:

**Claude (Anthropic):**
```bash
# Test via Claude.ai web interface
# Paste ai.md URL and prompt
```

**ChatGPT (OpenAI):**
```bash
# Test via ChatGPT interface
# Paste ai.md URL and prompt
```

**Gemini (Google):**
```bash
# Test via Gemini interface
# Paste ai.md URL and prompt
```

**Test matrix:**

| Model | Mode A Test | Mode B Test | Notes |
|-------|-------------|-------------|-------|
| Claude Sonnet 4 | ✅ / ❌ | ✅ / ❌ | |
| GPT-4o | ✅ / ❌ | ✅ / ❌ | |
| Gemini 2.0 | ✅ / ❌ | ✅ / ❌ | |

**Document any issues in GitHub Issues.**

#### 3.4 Backward Compatibility Test

Test that v0.1 prompts still work:

```bash
# Test an existing v0.1 prompt from /examples
# Verify it still works with v0.2 framework
```

**Potential issues:**
- Prompts with T = Target only (no Tone specified)
- Should still work, but may benefit from Tone addition

---

### Phase 4: Merge & Deploy (30 minutes)

#### 4.1 Create Pull Request

```bash
git push origin feat/v0.2-release
```

1. Go to GitHub repository
2. Create Pull Request: `feat/v0.2-release` → `main`
3. Add description:

```markdown
## CRAFTER v0.2 Release

### Major Changes
- **T Component Merge:** Target & Tone now integrated
- **Dual-Mode Capability:** Single entry point for enhancement and creation

### Files Added
- `ai.md` — Dual-mode AI briefing
- Updated `01-CRAFTER-SPEC.md`
- `example-mode-a-enhancement.md`
- `example-mode-b-creation.md`
- `IMPLEMENTATION_GUIDE.md`
- `QUICK_REFERENCE.md`

### Testing
- [x] Smoke tests passed (Mode A and Mode B)
- [x] Cross-model testing completed
- [x] Backward compatibility verified

### Breaking Changes
T component definition changed (Target only → Target & Tone)

See IMPLEMENTATION_GUIDE.md for full details.
```

4. Review files changed
5. Merge PR

#### 4.2 Tag Release

```bash
git checkout main
git pull origin main
git tag -a v0.2 -m "Release v0.2: Target & Tone merge + dual-mode capability"
git push origin v0.2
```

#### 4.3 Create GitHub Release

1. Go to Releases
2. Click "Draft a new release"
3. Select tag: `v0.2`
4. Title: `CRAFTER v0.2 — Target & Tone Integration`
5. Description:

```markdown
## What's New in v0.2

### Target & Tone Integration
The T component now combines Target (audience) and Tone (communication style) into a single, integrated component. This removes confusion and matches real-world communication design.

**Formula:** [Audience] + [Characteristics] → [Communication approach]

### Dual-Mode Capability
Single entry point (`ai.md`) now handles both:
- **Mode A:** Enhance existing prompts (restructure using CRAFTER)
- **Mode B:** Create new superprompts (generate from scratch)

### New Files
- `ai.md` — Unified AI briefing for both modes
- Updated `01-CRAFTER-SPEC.md` with v0.2 changes
- Example demonstrations for Mode A and Mode B
- Implementation guide and quick reference

See [IMPLEMENTATION_GUIDE.md](./IMPLEMENTATION_GUIDE.md) for deployment details.

### Breaking Changes
T component definition changed. Existing v0.1 prompts will benefit from adding Tone specification.
```

---

### Phase 5: Documentation Updates (30 minutes)

#### 5.1 Update Supporting Docs

Files that may need updates:

**docs/template.md:**
- Update T component definition
- Add Tone specification to template

**docs/quick-start.md:**
- Mention dual-mode capability
- Update T component examples

**docs/patterns.md:**
- Reference v0.2 where relevant

**docs/evaluation.md:**
- Add T = Target & Tone to checklist

#### 5.2 Update Links

Search for references to v0.1:
```bash
grep -r "v0.1" .
# Update to v0.2 where appropriate
```

---

## URL Strategy Options

### Option 1: GitHub-Only (Current)

**URL:** `https://github.com/CoachSteff/superprompt-framework`

**Pros:**
- No cost
- Already working
- Easy to maintain

**Cons:**
- Long URL
- Less memorable

### Option 2: Custom Domain (Recommended)

**Setup `sprompt.ai`:**

1. **Register domain** (Namecheap, Google Domains, etc.)
   - Cost: ~$12-30/year

2. **Set up redirect** via Cloudflare:
   - Add site to Cloudflare
   - Create Page Rule:
     - URL: `sprompt.ai/*`
     - Forwarding URL: `https://github.com/CoachSteff/superprompt-framework/$1`

3. **Benefits:**
   - Short, memorable URL
   - Professional branding
   - Easy to share ("Just go to sprompt.ai")

**Implementation time:** 30 minutes

### Option 3: GitHub Pages (Documentation Site)

**Setup:**

1. Create `docs/` branch
2. Build documentation site (MkDocs, Docusaurus, etc.)
3. Enable GitHub Pages
4. Point `sprompt.ai` to GitHub Pages

**Benefits:**
- Professional documentation site
- Better discoverability
- Custom styling

**Drawback:**
- More maintenance overhead

**Recommendation:** Start with Option 2 (custom domain with redirect), upgrade to Option 3 later if needed.

---

## Rollout Timeline

### Week 1: Soft Launch
- [ ] Deploy to GitHub
- [ ] Test with 3-5 early users
- [ ] Gather feedback
- [ ] Fix any critical issues

### Week 2: Public Announcement
- [ ] LinkedIn post about v0.2
- [ ] Update coachsteff.live
- [ ] Share in relevant communities
- [ ] Create tutorial video (optional)

### Week 3-4: Monitor & Iterate
- [ ] Track GitHub issues
- [ ] Collect user feedback
- [ ] Plan v0.3 features based on learnings

---

## Backward Compatibility

### Will v0.1 Prompts Still Work?

**Yes**, with caveats:

**Fully compatible:**
- All v0.1 prompts will continue to function
- No breaking changes to core structure

**Recommended updates:**
- Add Tone specification to T component
- Example: `Target: Marketing managers` → `Target: Marketing managers (action-oriented) | Tone: Direct, scannable`

### Migration Strategy

**Low priority:** Existing v0.1 prompts work fine, update when convenient

**High priority:** New prompts should use v0.2 format from day one

**Batch update:** Consider updating all examples in `/examples/` to v0.2 format for consistency

---

## Troubleshooting

### Issue: AI Not Detecting Mode Correctly

**Symptoms:** AI treats Mode A request as Mode B (or vice versa)

**Solutions:**
1. Check if user query clearly indicates mode (add examples to detection table)
2. Verify ai.md mode detection table is accurate
3. Ask user to be explicit: "Use Mode A to enhance this prompt"

### Issue: T Component Confusion

**Symptoms:** AI uses old T = Target only format

**Solutions:**
1. Update ai.md to emphasize v0.2 change
2. Add prominent callout: "CRITICAL: T = Target & Tone (v0.2 update)"
3. Include examples in every T component explanation

### Issue: Attribution Missing

**Symptoms:** Generated prompts lack attribution footer

**Solutions:**
1. Move attribution requirement higher in ai.md
2. Add to self-test checklist: "Attribution footer included?"
3. Make it bold/prominent in output format specification

---

## Success Metrics

Track these to evaluate v0.2 adoption:

**Usage metrics:**
- GitHub stars
- Repository forks
- ai.md file views
- Example file views

**Quality metrics:**
- Issue reports (bugs, confusion)
- Pull requests from community
- User testimonials

**Engagement metrics:**
- LinkedIn post engagement
- Website traffic (if using custom domain)
- Community questions/discussions

---

## Next Steps

After v0.2 is stable, consider:

### v0.3 Potential Features
- Pattern library expansion (add 5-10 new patterns)
- Integration templates (Cursor, GitHub Copilot, Cline)
- Video tutorials
- Interactive prompt builder tool

### Community Building
- Create Discord/Slack for users
- Host "Office Hours" sessions
- Build contributor community

### Documentation Expansion
- Case studies from real users
- Industry-specific examples
- Advanced techniques guide

---

## Questions & Support

**GitHub Issues:** https://github.com/CoachSteff/superprompt-framework/issues  
**Author:** Steff Vanhaverbeke ([@CoachSteff](https://github.com/CoachSteff))  
**Email:** steff@coachsteff.live  
**Website:** https://coachsteff.live

---

Framework: CoachSteff's CRAFTER (SuperPrompt Framework v0.2)  
License: CC-BY 4.0  
Last Updated: January 2025
