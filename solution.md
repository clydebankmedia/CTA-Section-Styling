# Solution Code - CTA Section Styling

<details>
<summary> Step 1 Solution - Center content and set container width</summary>
    
CSS - styles.css

```css
/* STEP 1: Center content and set container width */
/* styles.css */

/* Adds a readable line length, centers the layout, and adds inner padding */
.container {
  max-width: 680px;      /* keeps lines comfortable to read */
  margin: 0 auto;        /* centers the container in the viewport */
  padding: 32px 16px;    /* breathing room so text doesn't hug edges */
}
```

</details>

<details>
<summary>Step 2 Solution – Give the CTA block clear spacing</summary>

CSS - styles.css

```css
/* STEP 2: Give the CTA block clear spacing */
/* styles.css */

/* Separates the CTA from surrounding content and adds inner space */
.cta {
  margin: 32px 0;   /* space above and below the CTA block */
  padding: 24px;    /* comfortable inner spacing for text and button */
}
```

</details>  
<details>
<summary>Step 3 Solution – Style the button</summary>

CSS - styles.css

```css
/* STEP 3: Style the button */
/* styles.css */

/* Establishes button appearance and a comfortable click/tap target */
.btn {
  display: inline-block;      /* lets the link accept padding and size naturally */
  padding: 12px 16px;         /* accessible hit area on desktop and mobile */
  background: #2563eb;        /* high-contrast primary color */
  color: #fff;                /* readable text on the blue background */
  border-radius: 10px;        /* friendly, modern corners */
  border: 1px solid transparent; /* (optional) prevents layout shift if border changes later */
}
```

</details>   
<details>

<summary> Step 4 Solution – Add a button hover state</summary>

CSS - styles.css

```css
/* STEP 4: Add a button hover state */
/* styles.css */

/* Place this below the base .btn rule so it overrides correctly */
.btn:hover {
  filter: brightness(0.95); /* gentle darken to signal interactivity */
  transform: translateY(-1px); /* subtle lift to reinforce "this is clickable" */
}
```

</details>   



<details>

<summary> Step 5 Solution – Smooth hover transitions</summary>

CSS - styles.css

```css
/* STEP 5: Smooth hover transitions */
/* styles.css */

/* Add this inside the existing .btn rule from Step 3 (append these lines) */
.btn {
  /* ...existing Step 3 properties... */

  /* Animates the properties you change on hover so they glide, not snap */
  transition:
    filter 160ms ease,
    transform 160ms ease,
    box-shadow 160ms ease; /* harmless if no shadow yet; ready for Step 6 */
}
```

</details>   



<details>

<summary> Step 6 Solution (Optional Step) - Add gradient and soft shadow</summary>

CSS - styles.css

```css
/* STEP 6 (Optional): Add gradient and soft shadow */
/* styles.css */

/* Update the base button for subtle depth (replaces the solid background from Step 3) */
.btn {
  /* ...existing Step 3 base styles + Step 5 transition... */

  background: linear-gradient(to bottom, #3b82f6, #2563eb); /* soft vertical gradient */
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.08);               /* quiet depth under the button */
}

/* Strengthen the shadow slightly on hover to reinforce the lift */
.btn:hover {
  /* keep existing Step 4 hover effects (filter + transform) */
  box-shadow: 0 8px 18px rgba(0, 0, 0, 0.12); /* pairs with the lift from Step 4 */
}

```

</details>   



 



<details>
<summary>Final Solution</summary>

CSS - styles.css

```css
/* styles.css */

* { box-sizing: border-box; }
html, body { height: 100%; }
body {
  margin: 0;
  font-family: system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
  line-height: 1.5;
  color: #111827;
  background: #f8fafc;   /* page contrast */
}

/* CTA base card styles  */
.cta {
  background: #ffffff;
  border: 1px solid #e5e7eb;
  border-radius: 12px;
}

/* CTA font styles  */
.cta-title {
  margin: 0 0 8px 0;
  line-height: 1.2;
  font-size: 30px;
  font-weight: 700;
}
.cta-text {
  margin: 0 0 24px 0;
  color: #6b7280;
}

/* Footer  */
.site-footer {
  color: #6b7280;
  font-size: 14px;
  text-align: center;
  padding: 24px 0 48px;
}

/* =========================================
   1) YOUR WORK AREA (write CSS in step order)
   ========================================= */

/* STEP 1: Container centering + inner padding */
/* Adds a readable line length, centers the layout, and adds inner padding */
.container {
  max-width: 680px;      /* keeps lines comfortable to read */
  margin: 0 auto;        /* centers the container in the viewport */
  padding: 32px 16px;    /* breathing room so text doesn't hug edges */
}

/* STEP 2: CTA outside/inside spacing */
/* Separates the CTA from surrounding content and adds inner space */
.cta {
  margin: 32px 0;   /* space above and below the CTA block */
  padding: 24px;    /* comfortable inner spacing for text and button */
}

/* STEP 3: Button base (enables hover/transition) */
/* Establishes button appearance and a comfortable click/tap target */
.btn {
  display: inline-block;      /* lets the link accept padding and size naturally */
  padding: 12px 16px;         /* accessible hit area on desktop and mobile */
  background: #2563eb;        /* high-contrast primary color */
  color: #fff;                /* readable text on the blue background */
  border-radius: 10px;        /* friendly, modern corners */
  border: 1px solid transparent; /* (optional) prevents layout shift if border changes later */

  /* STEP 5: Smooth hover transitions */
  /* Animates the properties you change on hover so they glide, not snap */
  transition:
    filter 160ms ease,
    transform 160ms ease,
    box-shadow 160ms ease; /* harmless if no shadow yet; ready for Step 6 */

  /* STEP 6 (Optional): Gradient and soft shadow */
  background: linear-gradient(to bottom, #3b82f6, #2563eb); /* soft vertical gradient */
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.08);               /* quiet depth under the button */
}

/* STEP 4: Button hover feedback */
/* Place this below the base .btn rule so it overrides correctly */
.btn:hover {
  filter: brightness(0.95); /* gentle darken to signal interactivity */
  transform: translateY(-1px); /* subtle lift to reinforce "this is clickable" */

  /* STEP 6 (Optional): Strengthen shadow for the lift */
  box-shadow: 0 8px 18px rgba(0, 0, 0, 0.12); /* pairs with the lift from Step 4 */
}

```
</details>