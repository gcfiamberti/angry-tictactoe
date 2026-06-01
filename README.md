# angry-tictactoe
# Tic-tac-toe: a piece of cake or a piece of work?

A mobile-friendly conference demo for a tic tac toe experiment, with post-game ratings and Google Forms data collection.

## Overview

This repository contains a static website built to present one task from my experiment in a simple and accessible format. Visitors can play a short tic tac toe sequence on their smartphone, then report their experience using two sliders about enjoyment and frustration.

The website is hosted on GitHub Pages and shared through a direct link or QR code at a conference. It uses plain HTML, CSS, and JavaScript — no installation or backend server required.

## Website flow

1. Welcome page with a short introduction
2. Instructions page explaining the task and scoring
3. Game page with 10 tic tac toe matches against the computer
4. Feedback page with two sliders: enjoyment and frustration
5. Thank-you page shown after submitting the ratings

## Game logic

- The player is **X** and the computer is **O**
- 10 matches in total
- Wins give +1 point, losses give −1 point (minimum score: 0)
- Touch-based, designed for smartphone use
- Includes a covert deception mechanism from the original experimental task

## Data collection

Slider responses and game summary values are sent to a linked Google Form and stored automatically in a Google Sheet.

To activate this, replace the two placeholders in `index.html`:

```js
const GOOGLE_FORM_ACTION = 'PASTE_YOUR_GOOGLE_FORM_ACTION_URL_HERE';
const GOOGLE_FORM_FIELDS = {
  participantNumber: 'entry.REPLACE_NUMBER_FIELD',
  enjoyment:         'entry.REPLACE_ENJOYMENT_FIELD',
  frustration:       'entry.REPLACE_FRUSTRATION_FIELD',
  wins:              'entry.REPLACE_WINS_FIELD',
  losses:            'entry.REPLACE_LOSSES_FIELD',
  score:             'entry.REPLACE_SCORE_FIELD'
};
```

## Files
/
├── index.html ← main website
└── assets/
	├── API_transparent.svg
	└── Logo_IMT_School_vertical.jpg

## Editing text

All page text is marked inside `index.html` with comment tags:

```html
<!-- EDIT WELCOME TOP TEXT: start -->
...your text here...
<!-- EDIT WELCOME TOP TEXT: end -->
```

Search for `EDIT` to find every editable section.

---

**Author:** G. C. Fiamberti  
**Affiliation:** IMT School for Advanced Studies Lucca  
**Contact:** gaia.fiamberti@imtlucca.it
