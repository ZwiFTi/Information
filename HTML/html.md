# HTML

### Hvordan tenke

`<div>
  <p></p>
  <h1></h1>
  </div>`

 Her er div en parent til p, og p er en child av div. h1 er også en child av div, men en sibling til p.

### Begreper

- tree: A type of data in computer science
- div: Division element, used to group chunks of content together
- doctype:
- header: big important words
- hyperlink:
- a: anchor element
- href: reference
- paragraph: A big block of text that is seperate from other text
- span: A line of text that is not seperate from other text
- tag: `<p>` or `<h1>` etc
- element: `<p></p>` or `<h1></h1>` etc
- content: what goes inside elements
- opening tag: `<p>`
- closing tag: `</p>`
- attributes: describes the content of the page inside the html markup (`class` and `id`)

### Snippits

- [Setting the viewport](https://zerobin.net/?fb6e8c05962ef4f5#sVz0DTL8P8cjYUNUYHW91tZy02GJwNpPoPoLfbL7PKY=)

### Nyttig informasjon

- Et element har to tags, og teksten i taggene er alltid lik
- Klasser og id skal forklare elementet
- Bruk `id=""` når det bare er et element av en type
- Bruk `class=""` når man skal velge mange elements
- legg til flere classer ved å separere verdiene med mellomrom

### Reference pages

- MDN HTML element reference pages
- Udacity front end feedback
- HTML validator: https://validator.w3.org/#validate_by_input
- HTML Structural Elements: https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/Document_and_website_structure


### Checklist

1. HTML5 semantic tags such as <header>, <footer>, <article>, <section> etc. are used to add meaning to the code.
2. No <div> or <section> tags are without a CSS class or id.
3. Viewport meta er inkludert
4. It is acceptable to include height and width attributes in <img> elements.
5. All code is lowercase
6. No trailing white space
7. indentation consistency (2 vs 4) (space vs tabs)
8. only double quotation marks when quoting attributes
9. use HTML5 <!doctype html>
10. Code passes HTML validator.
11. html uses <meta charset="utf-8"> (No BOM)
12. Comments explain code: what it covers, what purpse it serves, the the solution is used and preferred
13. If you have stuff todo, mark with <!-- TODO: this -->
14. Do not close self-closing elements. (use <br> not <br />)
15. Multimedia has alternative content (alt="")
16. seperate html, css and js
17. do not use entity references
18. utelat type attributes like text/javascript
19. use a new line for every block, list or table element and indent every such child element
20.
