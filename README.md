# OOP Cheatsheet

Compact, interactive HTML cheatsheets explaining core Object-Oriented Programming (OOP) concepts in Dutch. This repository now contains two standalone HTML pages: one with JavaScript examples and one with PHP examples. Both files are self-contained and can be opened directly in a browser.

**Files**

- [cheatsheet-js.html](cheatsheet-js.html): OOP cheatsheet with JavaScript examples. Open directly in your browser.
- [cheatsheet-php.html](cheatsheet-php.html): OOP cheatsheet with PHP examples. Also standalone — open directly in your browser.

**Standalone usage**

- No server required: double-click either file or open it from your browser (`File → Open`) to view the cheatsheet.
- Optional: run a simple static server (e.g. `python -m http.server`) if you prefer `http://` access or remote testing.

**Features**

- Collapsible code blocks
- Copy-to-clipboard buttons for code examples.
- A small "ask chat" button that generates a pre-filled ChatGPT link for the selected section.
- Syntax highlighting using `highlight.js` (loaded from CDN in each page).

**Code blocks / languages**

- JavaScript examples use `class="language-javascript"` on the `<code>` element.
- PHP examples use `class="language-php"` on the `<code>` element.
- Keep the `class="code-content"` wrapper so the page JavaScript can attach copy/expand/chat buttons.

**Usage**

- Open the file directly (double-click) or open via your browser's `File → Open` dialog.
- To run a local static server (optional):

```bash
python -m http.server
```

**How to add content**

- **Add a new section:** Add a new `<li>` inside the top-level ordered list (`<ol>`). Follow the structure used elsewhere: a `<h3>` title, one or more `<p>` description paragraphs, and one or more code examples in `<pre>` blocks.
- **Add language-specific code blocks:** Use `<code class="language-javascript">...</code>` for JS or `<code class="language-php">...</code>` for PHP so highlight.js highlights correctly.
- **Minimal example - new section:**

```html
<li>
  <h3>Nieuwe Titel</h3>
  <p>Korte beschrijving van het onderwerp.</p>

  <pre class="code-content is-open">
    <code class="language-javascript">// Voorbeeldcode hier (JS)</code>

    or ...
    
    <code class="language-php">// Voorbeeldcode hier (PHP)</code>
  </pre>

  in case of extra info : 

  <p>Korte beschrijving van het onderwerp.</p>

  <pre class="code-content is-open">
    <code class="language-javascript">// Voorbeeldcode hier (JS)</code>

    or ...
    
    <code class="language-php">// Voorbeeldcode hier (PHP)</code>
  </pre>


</li>
```

**Development / Editing**

- Both HTML files include inline JavaScript that implements the buttons and collapsing behavior; `highlight.js` is loaded from a CDN inside each page.
- If you need offline highlighting, download `highlight.js` and update the script/style references in the HTML files.

**Author**

Repository created to accompany an OOP course (vdab) — keep it simple and editable. Feel free to open issues or edit the file directly.
