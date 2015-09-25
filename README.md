
# Atom snippets for Zurb Ink

Based on [ZURB Ink Sublime Snippets](https://github.com/christianrojas/zurb-ink-sublime-snippets)

| Module | Atom Prefix | Description  |
|:------------- | :------------- | :----------- |
| [Boilerplate](###Boilerplate) | zi-boilerplate |  Sets up your document |
| [Container](#Container) | zi-container | Wraps the content and maintains a fixed width  |
| [Row](#Row) | zi-row | Separates blocks of content vertically  |
| [Wrapper](#Wrapper) | zi-wrapper | Wraps hozitonal content inside a row  |
| [Columns](#Columns) | zi-columns | Go inside wrappers to determine width of content block  |
| [Sub-column](#Sub-column) | zi-sub-column | Sub-grid inside a column  |
| [Block](#Block) | zi-block | Even-width element grid that doesn't use media queries  |
| [Button](#Button) | zi-button | Empty button placeholder with documentation differnt Ink button styles  |
| [Image](#Image) | zi-image | Empty image placeholder with size documentation for different grid sizes |

—

### Boilerplate
```
<!DOCTYPE html PUBLIC “-//W3C//DTD XHTML 1.0 Strict//EN” “http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd”>
<html xmlns=“http://www.w3.org/1999/xhtml”>
  <head>
    <meta http-equiv=“Content-Type” content=“text/html; charset=utf-8” />
    <meta name=“viewport” content=“width=device-width”/>

    <link rel=“stylesheet” href=“email.css”> <!— For testing only - Remove when ready for css inlining —>

    <style type=“text/css”>

      /* copy email.css here before running through css inliner - http://zurb.com/ink/inliner.php */

    </style>
  </head>
  <body>
    <table class=“body”>
      <tr>
        <td class=“center” align=“center” valign=“top”>
          <center>

            <!— Email Content —>
            $1

          </center>
        </td>
      </tr>
    </table>
  </body>
</html>
```
---

### Container
```
<!-- Container -->

<table class="container">
  <tr>
    <td>
      $1
    </td>
  </tr>
</table>
```

---

### Row
```
<!-- Row -->

<table class="row">
  <tr>
    $1
  </tr>
</table>
```


---

### Wrapper
```
<!-- Wrapper -->

<td class="wrapper last">
  $1
</td>
```
---

### Columns
```
<!-- Columns -->

<!-- Visibility Classes: [show-for-small hide-for-small] -->
<!-- Size Classes: [one two three four five six seven eight nine ten eleven twelve] -->
<table class="$1size columns">
  <tr>
    <!-- Panel Class: [panel] -->
    <td>
      $2
    </td>
    <td class="expander"></td>
  </tr>
</table>
```
---

### Sub-column
```
<!-- Sub-Column -->

<!-- Visibility Classes: [show-for-small hide-for-small] -->
<!-- Size Classes: [one two three four five six seven eight nine ten eleven twelve] -->
<td class="$1size sub-columns last">
  $2
</td>
```
---

### Block
```
<!-- Block Grid -->

<!-- Block Size: [two-up three-up four-up five-up six-up seven-up eight-up] -->
<table class="block-grid $1block-size">
  <tr>
    <td>

      $2Column #1

    </td><td> <!-- Make sure the tags are directly next to each other -->

      $3Column #2

    </td>
  </tr>
</table>
```
---

### Button
```
<!-- Button -->

<!-- Size Classes:   [tiny-button small-button medium-button large-button] -->
<!-- Radius Classes: [radius round] -->
<!-- Color Classes:  [primary secondary alert success] -->
<table class="button">
  <tr>
    <td>
      <a href="$1">$2Button Name</a>
    </td>
  </tr>
</table>
```
---

### Image
```
<!-- Image -->

<!-- Size by Columns: [1:30 2:80 3:130 4:180 5:230 6:280 7:330 8:380 9:430 10:480 11:530 12:580] -->
<img height="$1" width="$2" src="$3">
```
