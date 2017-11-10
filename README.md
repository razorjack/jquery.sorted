Usage
=====

Example markup:

```html
<ul>
    <li data-id="9">one</li>
    <li data-id="8">two</li>
    <li data-id="7">three</li>
</ul>
```

Sorting by text value
---------------------

```javascript
$("ul li").sorted();
```

Result:

```html
<li data-id="9">one</li>
<li data-id="7">three</li>
<li data-id="8">two</li>
```

Reverse sorting
---------------

```javascript
$("ul li").sorted({
  reversed: true
});
```

Result:

```html
<li data-id="8">two</li>
<li data-id="7">three</li>
<li data-id="9">one</li>
```

Sorting by custom value
-----------------------

```javascript
$("ul li").sorted(
  {
    by: function(v) {
      return parseInt(v.attr('data-id'));
    }
  }
);
```

Result:

```html
<li data-id="7">three</li>
<li data-id="8">two</li>
<li data-id="9">one</li>
```
