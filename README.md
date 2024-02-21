# tiptap-extension-section

<h3 align="center">
    Make tiptap support section tags, which provide predefined styles for content.
</h3>

<br/>

<p align="center">
  <a href="https://www.npmjs.com/package/tiptap-extension-section">
    <img
     alt="NPM URL"
     src="https://img.shields.io/badge/npm-tiptapExtensionSection?logo=npm">
  </a>
  <img
     alt="version"
     src="https://img.shields.io/badge/version-1.0.0-blue">
</p>

<br>

---

## Install

```shell
npm install tiptap-extension-section -S
```

## Usage

```js
import Section from "tiptap-extension-section";

const editor = new Editor({
  element: document.querySelector(".editor"),
  extensions: [StarterKit, Section],
});
```

```js
const html = `
  <section style="display: flex;flex-direction: column;align-items: center;text-align: center;">
    <section style="color: #fff;border-radius: 4px;font-weight: bold;min-width: 30px;padding: 0 4px;line-height: 30px;background-color: grey;">
      <p>01</p>
    </section>
    <section style="color: grey">
      <p><strong>公司宣传手册</strong></p>
    </section>
    <section style="color: grey">
      <p>
        <span style="font-size: 12px">COMPANY BROCHURE</span>
      </p>
    </section>
  </section>`;
editor
  .chain()
  .focus()
  .insertContent(html, {
    parseOptions: {
      preserveWhitespace: false,
    },
  })
  .run();
```

## Relations

**tiptap-appmsg-editor:** https://github.com/KID-1912/tiptap-appmsg-editor
