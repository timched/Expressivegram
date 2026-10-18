# Expressivegram — Material 3 Expressive design direction

This document defines the intended UI direction for Expressivegram. It is a design target, not a claim that every component has already been converted.

## Principles

1. **Expressive, not decorative:** use shape, scale, color, and motion to establish hierarchy.
2. **One component language:** navigation, chat list, composer, dialogs, menus, settings, and media viewers should share the same tokens.
3. **Desktop ergonomics:** preserve efficient keyboard navigation, resizable layouts, hover/focus feedback, and compact options for dense workflows.
4. **Accessibility:** maintain readable contrast, visible focus, scalable text, and reduced-motion behavior.
5. **Incremental migration:** redesign component families and verify them before changing the next family.

## Initial token direction

| Token | Light theme direction | Dark theme direction |
|---|---|---|
| Primary | Deep violet / blue-violet | Soft violet |
| Surface | Warm near-white with subtle tonal layers | Deep charcoal with distinct elevated surfaces |
| Text | Near-black with clear secondary text | Near-white with readable secondary text |
| Shape | Rounded cards and expressive large surfaces | Same geometry, adjusted tonal separation |
| Motion | Short, purposeful transitions | Respect system reduced-motion preference |

Exact colors, corner radii, and timings should be centralized in the project's native C++/Qt style system rather than scattered through widgets.

## Implementation order

- [ ] Establish shared light/dark color and shape tokens.
- [ ] Redesign app navigation and chat list.
- [ ] Redesign message bubbles, composer, attachments, and reactions.
- [ ] Apply the same components to dialogs, menus, settings, and profile views.
- [ ] Review keyboard focus, accessibility contrast, and reduced motion.
- [ ] Add screenshots and UI regression checks.

## Engineering note

Telegram Desktop uses a substantial custom-painted C++/Qt UI and shared UI libraries. A stylesheet alone cannot faithfully convert the whole application; changes need to be made in the native components and their shared style definitions.
