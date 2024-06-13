---
author: Colin Gross
title: SVG
date: 2024-02-29
---

# Plotting
  - Javascript Library D3
  - Translate data space to figure space

## D3
  - Designed to visualize data
  - Tools to manipulate data
  - Tools to manipulate SVGs

## Display vs Data Coordinate Systems
First and significant hurdle to plotting data.

```svg
<svg id="c-demo" height=300 width=500>
```
```json
[ {name: "Datsun 710", mpg: 22.8, cyl: 4},
  {name: "Mazda RX4",  mpg: 21.0, cyl: 6},
  {name: "Valiant",    mpg: 18.1, cyl: 6},
  {name: "Camaro Z28", mpg: 13.3, cyl: 8} ]
```
```js
  let x_scale = d3.scaleLinear()
                  .domain([0,10]).range([30, 490]);
  let y_scale = d3.scaleLinear()
                  .domain([0,30]).range([30, 290]);
```

## Coordinate origin difference
- SVG origin is at the top left.
- People expect origin at the bottom left.

<svg id="c-demo" height=300 width=500>
  <rect id="bkgd" height="100%" width="100%" fill="lightgrey"/>
  <g id="points"></g>
  <g id="point-labs" style="font-size: 14px;"></g>
  <g id="axis-labs" style="font-size: 12px;">
    <text id="x-lab" transform="translate(230 15)" >cylinders</text>
    <text id="y-lab" transform="translate(10 180) rotate(-90)">mpg</text>
  </g>
  <g id="x-axis">
  </g>
  <g id="y-axis">
  </g>
</svg>

<script src="https://d3js.org/d3.v4.js"></script>
<script>
// MPG to Cylinders figure
  let mtcars = [
    {name: "Mazda RX4", mpg: 21.0, cyl: 6, disp: 160, hp: 110},
    {name: "Datsun 710", mpg: 22.8, cyl: 4, disp: 108, hp: 93},
    {name: "Valiant", mpg: 18.1, cyl: 6, disp: 225, hp: 105},
    {name: "Camaro Z28", mpg: 13.3, cyl: 8, disp: 350, hp:245} ];

  let x_scale = d3.scaleLinear()
                  .domain([0,10]).range([40, 490]);
  let y_scale = d3.scaleLinear()
                  .domain([0,30]).range([40, 290]);

  let points = d3.selectAll("#points").selectAll();
  let point_labs = d3.selectAll("#point-labs").selectAll();

  points.data(mtcars).enter()
    .append("circle")
    .attr("cx", d => x_scale(d.cyl))
    .attr("cy", d => y_scale(d.mpg))
    .attr("r", 2);

  point_labs.data(mtcars).enter()
    .append("text")
    .attr("x", d => x_scale(d.cyl))
    .attr("y", d => y_scale(d.mpg))
    .attr("transform", "translate(5 5)")
    .text(d => d.name);

  d3.selectAll("#x-axis")
    .attr("transform", "translate(0 40)")
    .call(d3.axisTop(x_scale));

  d3.selectAll("#y-axis")
    .attr("transform", "translate(40 0)")
    .call(d3.axisLeft(y_scale));
</script>


## Correct y-axis using reversed scale 

```js
let y_scale = d3.scaleLinear()
                .domain([0,30]).range([260, 10]);
```
<svg id="d2" height=300 width=500>
  <rect id="d2-bkgd" height="100%" width="100%" fill="lightgrey"/>
  <g id="d2-points"></g>
  <g id="d2-point-labs" style="font-size: 14px;"></g>
  <g id="d2-axis-labs" style="font-size: 12px;">
    <text id="d2-x-lab" transform="translate(230 290)" >cylinders</text>
    <text id="d2-y-lab" transform="translate(10 180) rotate(-90)">mpg</text>
  </g>
  <g id="d2-x-axis">
  </g>
  <g id="d2-y-axis">
  </g>
</svg>

Let the scales handle mapping data values to plotting space.
```js
    .attr("x", d => x_scale(d.cyl))
    .attr("y", d => y_scale(d.mpg))
```

<script>
let x_scale2 = d3.scaleLinear()
                .domain([0,10]).range([40, 490]);
let y_scale2 = d3.scaleLinear()
                .domain([0,30]).range([260, 10]);

let points2 = d3.selectAll("#d2-points").selectAll();
let point_labs2 = d3.selectAll("#d2-point-labs").selectAll();

points2.data(mtcars).enter()
  .append("circle")
  .attr("cx", d => x_scale2(d.cyl))
  .attr("cy", d => y_scale2(d.mpg))
  .attr("r", 2);

point_labs2.data(mtcars).enter()
  .append("text")
  .attr("x", d => x_scale2(d.cyl))
  .attr("y", d => y_scale2(d.mpg))
  .attr("transform", "translate(5 5)")
  .text(d => d.name);

d3.selectAll("#d2-x-axis")
  .attr("transform", "translate(0 260)")
  .call(d3.axisBottom(x_scale2));

d3.selectAll("#d2-y-axis")
  .attr("transform", "translate(40 -0)")
  .call(d3.axisLeft(y_scale2));
</script>
