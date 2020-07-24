## Simple custom select with pure css


```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Custom Select</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <div class="app-select">
      <select>
        <option value="">ReactJs</option>
        <option value="">Angular</option>
        <option value="">Vue</option>
        <option value="">NodeJs</option>
        <option value="">Express</option>
      </select>
      <span class="arrows"></span>
    </div>
  </body>
</html>
```

```css
body {
  margin: 0;
  min-height: 100vh;
  display: grid;
  place-items: center;
}
*{
    box-sizing: border-box;
}

.app-select {
  position: relative;
}
.app-select select {
  font-size: 1em;
  padding: 1em 4em 1em 1.5em;
  border: 0;
  background: #34495e;
  color: #fff;
  outline: none;
}
.app-select select option{
    border: 0;
    padding: 1.2em;
    background: #fff;
    color: #2c3e50;
    outline: none;
    display: block;
    padding: 2em;
}
.app-select .arrows {
  position: absolute;
  top: 0;
  right: 0;
  display: block;
  background: #2c3e50;
  height: 100%;
  width: 3em;
  pointer-events: none;
}

.app-select .arrows::before,
.app-select .arrows::after {
  --arrow-color: rgba(255, 255, 255, 0.7);
  --border-size: 0.6em;
  content: "";
  position: absolute;
  width: 0;
  height: 0;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.app-select .arrows::before {
  border-left: var(--border-size) solid transparent;
  border-right: var(--border-size) solid transparent;
  border-bottom: var(--border-size) solid var(--arrow-color);
  top: 37%;
}
.app-select .arrows::after {
  border-left: var(--border-size) solid transparent;
  border-right: var(--border-size) solid transparent;
  border-top: var(--border-size) solid var(--arrow-color);
  top: 63%;
}
```