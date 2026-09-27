# Web Programming – Lab 2

This assignment shows how one HTML page can look completely different when only its stylesheet changes. `index.html` contains six boxes (A–F), and two separate CSS files lay them out in two different ways.

## File Organization

```
web-programming-lab2/
├── index.html   # Page structure: a .container div holding six .box divs (A–F)
├── styleA.css   # Layout A: boxes stacked vertically and centered on the page
├── styleB.css   # Layout B: boxes placed side by side in a single horizontal row
└── README.md    # This file
```

## Challenges I Faced

- **Centering the text in the last box:** `text-align: center` only centers text horizontally. To center it vertically as well, I turned that box into a flex container with `align-items: center` and `justify-content: center`.
- **Keeping the boxes on one line in Layout B:** Inline-block elements wrapped to a new line on narrow screens, so I added `white-space: nowrap` to the container.
- **The fixed-position box:** After I set `position: fixed` on the last box, it no longer followed the other boxes in the row and could cover content. I also had to remove its right margin so it sat exactly in the corner.
