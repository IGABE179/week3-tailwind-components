# Tailwind Component Library

A small UI component library built with Tailwind CSS v4 utility classes: buttons, cards and alerts. Repeated class lists are extracted into reusable component classes with `@apply` in `src/style.css`, the only CSS file in the project.

**Author:** Olga Igabe

## Components

| Component | Classes | States / variants |
|---|---|---|
| Buttons | `.btn` + `.btn-primary`, `.btn-secondary`, `.btn-outline` | hover, active, focus-visible ring, disabled |
| Cards | `.card`, `.card-body`, `.card-title`, `.card-text` | profile card and product card (image, title, text, button), hover shadow |
| Alerts | `.alert` + `.alert-success`, `.alert-warning`, `.alert-error`, `.alert-info` | four colour types |

Custom theme colours (`navy`, `mist`, `gold`) are defined with `@theme` in the same file.

## Run locally

    npm install
    npm run dev

Then open the address Vite prints (usually http://localhost:5173).

## Group members

I joined the programme after the group sessions had taken place, so I completed this assignment on my own.

## Trade-off: `@apply` component classes vs utilities in the HTML

Writing every utility directly in the HTML makes each element's styling visible in one place and easy to change for one element, but long class lists get repeated on every button and become hard to keep consistent. Moving them into `.btn-primary` or `.alert-error` with `@apply` keeps the HTML short and means one change updates every button, but the styles now live in a separate file, so you have to open the CSS to see what a class does. I used `@apply` only for components that repeat (buttons, cards, alerts) and kept one-off layout utilities such as grids and spacing in the HTML.

