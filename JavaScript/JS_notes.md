# JavaScript:
## In-file JS:
- Using Script Tags to implement Js in a HTML file
  - Unorganized and confusing (cluttered)
  - Code is not reusable

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React Tutorial</title>
  </head>
  <body>
    <script type="text/javascript">
      // Comment Type1 (Single line)
      
      /* Multiple
      Line
      Comment*/
      
      document.write("Hello World")                     // Prints out Hello World on the WB
    </script>
  </body>
</html>
```

## Using External Files:
- Sript tag is used to point to the source of the Javascript
  - More organized ad you only have to change the code in the JS File
  - Reusable code

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React Tutorial</title>
    <!-- Add the script tag to the head tag-->
    <script src = "index.js"></script>
  </head>
  <body>
    
  </body>
</html>
```
```js
      alert("The file is working")                    // Prints out an alert in the WB with the perticular message
```

## Writing HTML using JS:

