# MUST Applications: Login and Account Creation (design prototype)

Course unit: Internet Technology and Web Design (Software Engineering)
Technologies: HTML5 and CSS only (no JavaScript, no frameworks)

## Files

| File | What it is |
|---|---|
| `login.html` | Login screen (email + 6-digit access code) |
| `register.html` | Account creation screen |
| `styles.css` | One shared stylesheet for both screens |

To view: put all three files in the same folder and open `login.html` in a browser.
The two pages link to each other ("Create an account" / "Log in").

## How the design follows the MUST application guidelines

Researched from the MUST admissions pages and the official portal guide:

- Applicants sign up with an **email address and phone number**.
- A temporary **6-digit access code** is sent to **both** phone and email, because SMS can be delayed. The login screen asks for email + access code.
- Applicants without a code are sent to account creation (as on the real portal).
- After login the applicant chooses a scheme, pays the form fee, then submits documents. This is shown as the 4-step route in the left panel.
- Fees differ for Ugandan/EAC and international applicants, so account creation asks which group the applicant belongs to.
- MUST warns that false information cancels admission, so the sign-up form includes a confirmation checkbox.
- MUST name, full university name and admissions contact details appear on both pages.

## Original design ideas

- **Application route:** the left panel shows the whole process as a numbered vertical route with a gold marker on the current step (step 2 on login, step 1 on account creation). Numbers are used because the process is a true sequence.
- **Split screen:** brand and process on the left, a quiet form on the right, identical on both pages so they feel like one system.
- **Palette:** deep teal, cool paper white, one gold accent. All colours are CSS variables at the top of `styles.css`.
- **Wordmark:** an original "M" tile, not the official MUST logo.

## HTML5 features used

Semantic elements (`aside`, `main`, `section`, `footer`, `ol`), `fieldset`/`legend`, input types (`email`, `tel`, `password`), `required`, `pattern`, `minlength`/`maxlength`, `inputmode`, `autocomplete`, `aria-current`, `aria-describedby`.

## CSS features used

Custom properties (design tokens), CSS Grid and Flexbox, CSS counters (route numbers), pseudo-elements, `:focus-visible`, `:user-invalid`, `:checked + span` (custom radio buttons), media queries (tablet and phone layouts), `prefers-reduced-motion`.

## Accessibility

Every input has a label; visible keyboard focus; touch-friendly input height; text contrast checked against the palette; layout works from 320px wide up; animation is minimal and switched off for users who request it.

## Limits

This is a front-end prototype. Forms use `action="#"`, so nothing is sent or stored. It is not the official MUST portal; the real one is at https://applications.must.ac.ug.
