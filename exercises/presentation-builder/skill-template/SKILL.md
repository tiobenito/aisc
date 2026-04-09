---
name: make-deck
description: "Turn rough notes, bullet points, or a topic into a polished HTML slide deck. Use when user says 'make a deck', 'create a presentation', 'turn these notes into slides', 'build a deck', or 'slide deck from these notes'."
allowed-tools: ["Read", "Write", "Bash", "Glob", "Edit"]
---

# Make Deck

Turns rough notes or bullet points into a polished HTML slide deck that opens in any browser.

## Workflow

1. Read the slide template from `~/.claude/skills/make-deck/references/slide-template.html`
2. Read the user's input (rough notes, bullet points, or topic). If the user hasn't provided notes yet, ask for them.
3. Structure the content into slides:
   - **Title slide**: presentation title + subtitle + today's date
   - **3-6 content slides**: one key idea per slide, with bullet points or short text
   - **Closing slide**: summary, next steps, or call to action
4. Generate the HTML deck using the template structure and styling. Keep the full CSS and JavaScript from the template.
5. Save the deck to the current directory as `[topic-slug]-deck.html` (e.g., `q1-update-deck.html`)
6. Tell the user the file path and suggest they open it in a browser.
7. After the user reviews, iterate on feedback. If they correct or adjust anything, append a learning to `~/.claude/skills/make-deck/learnings.md`.

## Style Rules

- **One idea per slide.** If a slide has more than one main point, split it.
- **Bullets over paragraphs.** Max 4-5 bullets per slide. Each bullet under 15 words.
- **Title slide is always dark background.** Content slides are light.
- **No filler slides.** Every slide should earn its place.
- **Keep it to 5-8 slides total.** Short decks are better decks.
- **Use the template's styling exactly.** Don't invent new CSS.

## What NOT to Do

- Don't add images or external dependencies
- Don't create slides with walls of text
- Don't use more than 8 slides unless the user explicitly asks
- Don't skip the title slide or closing slide
