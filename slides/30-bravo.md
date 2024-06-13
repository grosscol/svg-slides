---
author: Colin Gross
title: SVG
date: 2024-06-13
---

# BRAVO use of SVG
  - Sequence Depth 
  - Transcript Location
  - Variant Count

## Plotting Depth

Coverage data emitted by API for a region:
```json
{ "chrom": "1", "end": 50185001, "mean": 36.3528, "start": 50185000 },
{ "chrom": "1", "end": 50185004, "mean": 35.9806, "start": 50185002 },
{ "chrom": "1", "end": 50185005, "mean": 36.4722, "start": 50185005 },
{ "chrom": "1", "end": 50185011, "mean": 36.1583, "start": 50185006 },
{ "chrom": "1", "end": 50185013, "mean": 36.2833, "start": 50185012 },
{ "chrom": "1", "end": 50185017, "mean": 36.1222, "start": 50185014 },
{ "chrom": "1", "end": 50185018, "mean": 36.6639, "start": 50185018 },
{ "chrom": "1", "end": 50185019, "mean": 36.075, "start": 50185019 },
{ "chrom": "1", "end": 50185020, "mean": 36.7889, "start": 50185020 },
{ "chrom": "1", "end": 50185022, "mean": 35.9389, "start": 50185021 },
{ "chrom": "1", "end": 50185023, "mean": 36.6417, "start": 50185023 },
{ "chrom": "1", "end": 50185026, "mean": 35.8694, "start": 50185024 },
{ "chrom": "1", "end": 50185027, "mean": 46.3778, "start": 50185027 },
{ "chrom": "1", "end": 50185028, "mean": 46.1444, "start": 50185028 },
{ "chrom": "1", "end": 50185030, "mean": 46.5, "start": 50185029 },
{ "chrom": "1", "end": 50185032, "mean": 46.0417, "start": 50185031 },
{ "chrom": "1", "end": 50185033, "mean": 46.3806, "start": 50185033 },
{ "chrom": "1", "end": 50185039, "mean": 45.8056, "start": 50185034 },
{ "chrom": "1", "end": 50185042, "mean": 45.4833, "start": 50185040 },
{ "chrom": "1", "end": 50185044, "mean": 35.95, "start": 50185043 },
{ "chrom": "1", "end": 50185046, "mean": 35.3972, "start": 50185045 },
{ "chrom": "1", "end": 50185053, "mean": 35.9722, "start": 50185047 },
{ "chrom": "1", "end": 50185054, "mean": 35.3389, "start": 50185054 },
{ "chrom": "1", "end": 50185055, "mean": 35.625, "start": 50185055 },
{ "chrom": "1", "end": 50185056, "mean": 15.5278, "start": 50185056 },
{ "chrom": "1", "end": 50185057, "mean": 16.0111, "start": 50185057 },
```

## Use a path

- Instructions to follow go from one point to another.
- Useful for complex geometries and dense data.
- Difficult to read syntax

```svg
<path
d="M40,71.1647659574468
L52.69230769230769,71.1647659574468
L52.69230769230769,73.30293617021275
L71.73076923076923,73.30293617021275
L71.73076923076923,70.47885106382978
L78.07692307692308,70.47885106382978
L78.07692307692308,72.28210638297875
L116.15384615384616,72.28210638297875
L116.15384615384616,71.56402127659575
L128.84615384615384,71.56402127659575
L128.84615384615384,72.48948936170211
L154.23076923076923,72.48948936170211
L154.23076923076923,69.37759574468086
L160.57692307692307,69.37759574468086
L160.57692307692307,72.76063829787233
L166.92307692307693,72.76063829787233
L166.92307692307693,68.65951063829789
L173.26923076923077,68.65951063829789
L173.26923076923077,73.54248936170214
L185.96153846153845,73.54248936170214
L185.96153846153845,69.50512765957447
L192.30769230769232,69.50512765957447
L192.30769230769232,73.94174468085106
L211.34615384615387,73.94174468085106
L211.34615384615387,13.574340425531943
L217.69230769230768,13.574340425531943
L217.69230769230768,14.915148936170226
L224.03846153846155,14.915148936170226
L224.03846153846155,12.872340425531888
L236.73076923076923,12.872340425531888
L236.73076923076923,15.505127659574498
L249.4230769230769,15.505127659574498
L249.4230769230769,13.558255319148941
L255.76923076923077,13.558255319148941
L255.76923076923077,16.861446808510607
L293.84615384615387,16.861446808510607
L293.84615384615387,18.712957446808502
L312.88461538461536,18.712957446808502
L312.88461538461536,73.4787234042553
L325.5769230769231,73.4787234042553
L325.5769230769231,76.65438297872342
L338.2692307692308,76.65438297872342
L338.2692307692308,73.3511914893617
L382.69230769230774,73.3511914893617
L382.69230769230774,76.98929787234042
L389.03846153846155,76.98929787234042
L389.03846153846155,75.34574468085106
L395.38461538461536,75.34574468085106
L395.38461538461536,190.79774468085105
L401.7307692307693,190.79774468085105
L401.7307692307693,188.02134042553192
L408.0769230769231,188.02134042553192
L408.0769230769231,190.54268085106384
L420.7692307692307,190.54268085106384
L420.7692307692307,188.99448936170214
L535,188.99448936170214
L535,192.13855319148936
L554.0384615384615,192.13855319148936
L554.0384615384615,194.5955531914894
L560.3846153846154,194.5955531914894
L560.3846153846154,78.21808510638297
L573.0769230769231,78.21808510638297
L573.0769230769231,79.89380851063831
L649.2307692307693,79.89380851063831
L649.2307692307693,79.15963829787233
L655.5769230769231,79.15963829787233
L655.5769230769231,81.71257446808511
L693.6538461538462,81.71257446808511
L71.73076923076923,280
L52.69230769230769,280
L52.69230769230769,280
L40,280Z">
</path>
```

## D3 Library line generator

Handy function for generating path's commands.

```js
let line_gen = d3.line()
  .x(d => x_pos_scale(d.start))
  .y(d => y_depth_scale(d.mean))
  .curve(d3.curveStepAfter);
```

Can then be applied to given data.

```js
d3.select("#depth-line").selectAll()
  .data([cov_data])
  .enter()
  .append("path")
    .style("stroke-width", 1)
    .style("stroke", "red")
    .style("fill", "none")
    .attr('d', line_gen);
```

## Path in Action

<svg id="p-demo" height=300 width=700>
  <rect id="bkgd" height="100%" width="100%" fill="lightgrey"/>
  <clipPath id="depth-clip">
    <rect x="0%" y="0%" width="100%" height="100%"></rect>
  </clipPath>
  <rect id="bkgd" height="100%" width="100%" fill="lightgrey"/>
  <g id="depths"></g>
  <g id="dtop"></g>
  <g id="axis-labs" style="font-size: 12px;">
    <text transform="translate(10 180) rotate(-90)">depth</text>
  </g>
  <g id="pos-axis"></g>
  <g id="depth-axis"></g>
</svg>

<script>
let cov_data = [
  { "chrom": "1", "end": 50185001, "mean": 36.3528, "start": 50185000 },
  { "chrom": "1", "end": 50185004, "mean": 35.9806, "start": 50185002 },
  { "chrom": "1", "end": 50185005, "mean": 36.4722, "start": 50185005 },
  { "chrom": "1", "end": 50185011, "mean": 36.1583, "start": 50185006 },
  { "chrom": "1", "end": 50185013, "mean": 36.2833, "start": 50185012 },
  { "chrom": "1", "end": 50185017, "mean": 36.1222, "start": 50185014 },
  { "chrom": "1", "end": 50185018, "mean": 36.6639, "start": 50185018 },
  { "chrom": "1", "end": 50185019, "mean": 36.075, "start": 50185019 },
  { "chrom": "1", "end": 50185020, "mean": 36.7889, "start": 50185020 },
  { "chrom": "1", "end": 50185022, "mean": 35.9389, "start": 50185021 },
  { "chrom": "1", "end": 50185023, "mean": 36.6417, "start": 50185023 },
  { "chrom": "1", "end": 50185026, "mean": 35.8694, "start": 50185024 },
  { "chrom": "1", "end": 50185027, "mean": 46.3778, "start": 50185027 },
  { "chrom": "1", "end": 50185028, "mean": 46.1444, "start": 50185028 },
  { "chrom": "1", "end": 50185030, "mean": 46.5, "start": 50185029 },
  { "chrom": "1", "end": 50185032, "mean": 46.0417, "start": 50185031 },
  { "chrom": "1", "end": 50185033, "mean": 46.3806, "start": 50185033 },
  { "chrom": "1", "end": 50185039, "mean": 45.8056, "start": 50185034 },
  { "chrom": "1", "end": 50185042, "mean": 45.4833, "start": 50185040 },
  { "chrom": "1", "end": 50185044, "mean": 35.95, "start": 50185043 },
  { "chrom": "1", "end": 50185046, "mean": 35.3972, "start": 50185045 },
  { "chrom": "1", "end": 50185053, "mean": 35.9722, "start": 50185047 },
  { "chrom": "1", "end": 50185054, "mean": 35.3389, "start": 50185054 },
  { "chrom": "1", "end": 50185055, "mean": 35.625, "start": 50185055 },
  { "chrom": "1", "end": 50185056, "mean": 15.5278, "start": 50185056 },
  { "chrom": "1", "end": 50185057, "mean": 16.0111, "start": 50185057 },
  { "chrom": "1", "end": 50185059, "mean": 15.5722, "start": 50185058 },
  { "chrom": "1", "end": 50185077, "mean": 15.8417, "start": 50185060 },
  { "chrom": "1", "end": 50185080, "mean": 15.2944, "start": 50185078 },
  { "chrom": "1", "end": 50185081, "mean": 14.8667, "start": 50185081 },
  { "chrom": "1", "end": 50185083, "mean": 35.125, "start": 50185082 },
  { "chrom": "1", "end": 50185095, "mean": 34.8333, "start": 50185084 },
  { "chrom": "1", "end": 50185096, "mean": 34.9611, "start": 50185096 },
  { "chrom": "1", "end": 50185102, "mean": 34.5167, "start": 50185097 },
  { "chrom": "1", "end": 50185103, "mean": 34.0444, "start": 50185103 },
  { "chrom": "1", "end": 50185106, "mean": 34.4611, "start": 50185104 }];

let max_depth = Math.ceil(d3.max(cov_data, d => d.mean));
let max_pos = d3.max(cov_data, d => d.start);
let min_pos = d3.min(cov_data, d => d.start);

let x_pos_scale = d3.scaleLinear().domain([min_pos,max_pos]).range([40, 700]);
let y_depth_scale = d3.scaleLinear().domain([0, max_depth]).range([280, 10]); 

let cov_area = d3.area()
  .x(  d  => x_pos_scale(d.start) )
  .y0( () => 0)
  .y1( () => 0)
  .y0( () => 280 )
  .y1( d  => y_depth_scale(d.mean) )
  .curve(d3.curveStepAfter);

d3.select("#depths").selectAll()
   .data([cov_data])
   .enter()
  .append("path")
    .style("fill", "#ffa37c")
    .style("opacity", "50%")
    .style("stroke-width", 0.1)
    .style("stroke", "black")
    .attr("id","depths-path")
    .attr("clip-path", "url(#depth-clip)")
    .attr("d", cov_area);

d3.selectAll("#depth-axis")
  .attr("transform", "translate(40 0)")
  .call(d3.axisLeft(y_depth_scale));

/* line generator */
const line = d3.line()
  .x(d => x_pos_scale(d.start))
  .y(d => y_depth_scale(d.mean))
  .curve(d3.curveStepAfter);
  
let tracer = d3.selectAll("#dtop").selectAll()
  .data([cov_data])
  .enter()
  .append("path")
    .style("stroke-width", 1)
    .style("stroke", "red")
    .style("fill", "none")
    .attr('d', line);

const length = tracer.node().getTotalLength();

function reptrace() {
  tracer.attr("stroke-dasharray", length + " " + length)
        .attr("stroke-dashoffset", length)
          .transition()
          .ease(d3.easeLinear)
          .attr("stroke-dashoffset", 0)
          .duration(6000)
          .on("end", () => setTimeout(reptrace, 1000));
};

reptrace();

</script> 
