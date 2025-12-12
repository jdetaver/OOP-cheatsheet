# OOP Cheatsheet

A compact, interactive HTML cheatsheet explaining core Object-Oriented Programming (OOP) concepts in Dutch. The repository contains a single interactive page with code examples, syntax highlighting, and small UI helpers for copying code and collapsing/expanding examples.

**Files**

- `cheatsheet.html`: The main (and only) file. Open it in a browser to view the cheatsheet.

**Features**

- Collapsible code blocks (the page starts with many blocks collapsed by default).
- Copy-to-clipboard buttons for code examples.
- A small "ask chat" button that generates a pre-filled ChatGPT link for the selected section.
- Syntax highlighting using `highlight.js` (loaded from CDN in the page).

**Usage**

- Open the cheatsheet locally by double-clicking `cheatsheet.html`

- Each code example is wrapped like this:

```html
<pre class="code-content is-open">
  <code class="language-javascript">// code here</code>
</pre>
```

- To have a code block collapsed by default, add the `default_collapsed` class:

```html
<pre class="code-content is-open default_collapsed"> ... </pre>
```

**Development / Editing**

- The page uses CDN-hosted `highlight.js` for code coloring; you can replace or pin the version if you prefer offline usage.
- Buttons and collapsing behavior are implemented in the inline JavaScript at the top of `cheatsheet.html`.

**How to add content**

- **Add a new section:** Add a new list item (`<li>`) inside the top-level ordered list (`<ol>`). The new `<li>` should follow the same structure used in the file — a `<h3>` title, one or more `<p>` description paragraphs, and one or more code examples in `<pre>` blocks. See the example starting at line 363 in `cheatsheet.html` for the exact structure and ordering.

- **Add an extra block to an existing section:** To expand an existing section, add a new paragraph (`<p>`) and then a `<pre class="code-content ..."><code class="language-javascript">...</code></pre>` block immediately after it. This pattern (paragraph + pre/code block) is demonstrated starting on line 394 in `cheatsheet.html`.

- **Minimal example - new section:**

```html
<li>
  <h3>Nieuwe Titel</h3>
  <p>Korte beschrijving van het onderwerp.</p>
  <pre class="code-content is-open">
    <code class="language-javascript">// Voorbeeldcode hier</code>
  </pre>
</li>
```

- **Minimal example - extra block in existing section:**

```html
<p>Extra uitleg of uitdiepingstekst.</p>
<pre class="code-content is-open default_collapsed">
  <code class="language-javascript">// Meer voorbeeldcode hier</code>
</pre>
```

- When adding code blocks, keep the `class="code-content"` and `class="language-javascript"` conventions so the built-in JavaScript can attach the copy/expand/chat buttons and highlight.js can style the code.


**Author**

Repository created to accompany an OOP course (vdab) — keep it simple and editable. Feel free to open issues or edit the file directly.
