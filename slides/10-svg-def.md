---
author: Colin Gross
title: SVG
date: 2024-02-29
---

# SVG Format
Image format based on XML.
Open standard developed for the web.

## Describes Geometries and Styling

```svg
<svg height="100" width="100">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle r="45" cx="50" cy="50" fill="green" />
</svg> 
```
<svg height="100" width="100">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle r="45" cx="50" cy="50" fill="green" />
</svg> 


## Scaling

Same content with different image sizes scales without quality loss.

```svg
<svg height="25" width="25">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle r="45%" cx="50%" cy="50%" fill="green" />
</svg> 

<svg height="150" width="150">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle r="45%" cx="50%" cy="50%" fill="green" />
</svg> 

<svg height="500" width="500">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle r="45%" cx="50%" cy="50%" fill="green" />
</svg> 
```

## Scaling

<svg height="25" width="25">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle r="45%" cx="50%" cy="50%" fill="green" />
</svg> 

<svg height="150" width="150">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle r="45%" cx="50%" cy="50%" fill="green" />
</svg> 

<svg height="500" width="500">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle r="45%" cx="50%" cy="50%" fill="green" />
</svg> 

## DOM Accessible

<script>
function changeColor(){
  let circle = document.getElementById("my-circle");
  console.log(circle.style.fill);
  if(circle.style.fill === "lightgreen"){
    circle.style.fill = "green";
  }else{
    circle.style.fill = "lightgreen";
  }
}
</script>

SVG elements are accessible and manipulatable as part of a document model.

<svg height="100" width="200">
  <rect height="100%" width="100%" fill="#7ecadf"/>
  <circle id="my-circle" r="45%" cx="50%" cy="50%" fill="green" />
</svg> 
<button onclick="changeColor()">Toggle Color</button>

```js
function toggleColor(){
  let circle = document.getElementById("my-circle");

  if(circle.style.fill === "lightgreen"){
    circle.style.fill = "green";
  }else{
    circle.style.fill = "lightgreen";
  }
}
```

