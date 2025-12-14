# FUTO Keyboard Research Notes

**Date:** 2025-12-14  
**Purpose:** Technical feasibility assessment for NationOS Covenant Keyboard

---

## Repository Information

- **GitHub:** https://github.com/futo-org/android-keyboard
- **Primary Source:** https://gitlab.futo.org/keyboard/latinime (internal GitLab, mirrored to GitHub)
- **Website:** https://keyboard.futo.org/
- **License:** FUTO Source First License 1.1-kb
- **Base:** Fork of LatinIME (Android Open-Source Keyboard)

## Architecture Overview

### Technology Stack
- **Primary Languages:** C++ (59.5%), Java (24.4%), Kotlin (9.3%), C (6.4%)
- **Build System:** Gradle
- **Platform:** Android

### Key Components
- **Dictionaries:** Offline dictionary system
- **Native:** C/C++ core keyboard logic
- **Voice Input:** Integrated voice-to-text (separate shared module)
- **Translations:** Submodule for internationalization
- **Libs:** External libraries as submodule
- **Layouts:** Separate repository for keyboard layouts (Apache 2.0 license)

### Features
- Swipe typing
- Autocorrect
- Predictive text
- Voice input
- Fully offline operation
- Privacy-focused (no internet connection required)

## Licensing Analysis

### FUTO Source First License 1.1-kb

**Key Terms:**
- **Use:** Any purpose allowed
- **Modification:** Only for non-commercial purposes (personal use, research, testing, religious observance, hobby projects)
- **Distribution:** Free of charge for non-commercial purposes only
- **Payment Functionality:** Cannot remove or obscure payment-related functionality
- **Notices:** Must preserve licensing and copyright notices
- **Trademarks:** Subject to applicable law

**Critical Limitation:**
> "You may modify the software only for non-commercial purposes such as personal use for research, experiment, and testing for the benefit of public knowledge, personal study, private entertainment, hobby projects, amateur pursuits, or religious observance, all without any anticipated commercial application."

**Implication for NationOS:**
- The license allows modification for "religious observance" which aligns with our covenant-centric mission
- Distribution must be free of charge for non-commercial purposes
- Cannot sell the keyboard commercially
- Must preserve FUTO payment functionality (or work around this limitation)

## Contribution Requirements

- **CLA:** Contributor License Agreement required for pull requests to main repo
- **Layouts:** No CLA required for layout contributions (Apache 2.0)
- **Translation:** Via Pontoon instance at https://i18n-keyboard.futo.org/

## Build Process

```bash
# Recursive clone required
git clone --recursive https://gitlab.futo.org/keyboard/latinime.git

# Or fetch submodules after clone
git submodule update --init --recursive

# Build commands
./gradlew assembleUnstableDebug
./gradlew assembleStableRelease
```

## Modification Points for Covenant Keyboard

Based on the architecture, key modification points would be:

1. **AI Integration:** Modify the autocorrect/predictive text system to integrate local LLM
2. **Media Gallery:** Replace GIF/emoji libraries in the resources
3. **Clipboard:** Extend clipboard functionality with encryption and P2P sharing
4. **Tool Integration:** Add custom buttons/actions for wallet integration, message signing
5. **Theming:** Covenant-centric visual design and branding

---

**Conclusion:** FUTO Keyboard provides a solid, privacy-focused foundation. The license allows modification for religious observance, which aligns with our mission. The main constraint is the non-commercial distribution requirement, which is acceptable for the NationOS ecosystem.
