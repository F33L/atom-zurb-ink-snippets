
# Atom snippets for Zurb Ink

Collection of snippets to make using [Zurb Ink v1.0.5](http://zurb.com/ink/) easier

Based on [ZURB Ink Sublime Snippets](https://github.com/christianrojas/zurb-ink-sublime-snippets)

---
### Installation
- In Atom: File > Open Your Snippets
- Copy the contents of atom-ink-snippets.cson into snippets.cson
- Type one of the Atom Prefixes below (ex: zi-boilerplate) in an HTML document and press tab

---
### Snippets
| Module | Atom Prefix | Description  |
|:------------- | :------------- | :----------- |
| [Boilerplate](#boilerplate) | zi-boilerplate |  Sets up your document |
| [Container](#Container) | zi-container | Wraps the content and maintains a fixed width  |
| [Row](#Row) | zi-row | Separates blocks of content vertically  |
| [Wrapper](#Wrapper) | zi-wrapper | Wraps hozitonal content inside a row  |
| [Columns](#Columns) | zi-columns | Go inside wrappers to determine width of content block  |
| [Sub-column](#Sub-column) | zi-sub-column | Sub-grid inside a column  |
| [Block](#Block) | zi-block | Even-width element grid that doesn't use media queries  |
| [Button](#Button) | zi-button | Empty button placeholder with button style documentation  |
| [Image](#Image) | zi-image | Empty image placeholder with sizing documentation |

---

#### <a name="boilerplate"></a>Boilerplate 
[Ink Documentation](http://zurb.com/ink/docs.php#start)
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

#### <a name="Container"></a>Container
[Ink Documentation](http://zurb.com/ink/docs.php#grid)
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

### <a name="Row">Row
[Ink Documentation](http://zurb.com/ink/docs.php#grid)
```
<!-- Row -->

<table class="row">
  <tr>
    $1
  </tr>
</table>
```


---

#### <a name="Wrapper"></a>Wrapper
[Ink Documentation](http://zurb.com/ink/docs.php#grid)
```
<!-- Wrapper -->

<td class="wrapper last">
  $1
</td>
```
---

#### <a name="Columns"></a>Columns
[Ink Documentation](http://zurb.com/ink/docs.php#grid)
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

#### <a name="Sub-column"></a>Sub-column
[Ink Documentation](http://zurb.com/ink/docs.php#sub-grid)
```
<!-- Sub-Column -->

<!-- Visibility Classes: [show-for-small hide-for-small] -->
<!-- Size Classes: [one two three four five six seven eight nine ten eleven twelve] -->
<td class="$1size sub-columns last">
  $2
</td>
```
---

#### <a name="Block"></a>Block
[Ink Documentation](http://zurb.com/ink/docs.php#block-grid)
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

#### <a name="Button"></a>Button
[Ink Documentation](http://zurb.com/ink/docs.php#buttons)
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

#### <a name="Image"></a>Image
[Ink Documentation](http://zurb.com/ink/docs.php#images)
```
<!-- Image -->

<!-- Size by Columns: [1:30 2:80 3:130 4:180 5:230 6:280 7:330 8:380 9:430 10:480 11:530 12:580] -->
<img height="$1" width="$2" src="$3">
```
