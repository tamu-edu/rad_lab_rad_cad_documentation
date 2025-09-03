# Flat Isogrid Feature

<p align="left">
  <img src="/demo-images/flat-iso1.png" width="225">
  <img src="/demo-images/flat-iso2.png" width="175">
  <img src="/demo-images/flat-iso3.png" width="260">
</p>

## Feature Overview

The flat isogrid feature automatically cuts isogrid into a flat surface. There are many ways this can be customized to be at different angles, with different sized isogrid patterns, or different types of cutting. 

The perimeter of the face isogrid is being added to cannot involve a spline or the isogrid will not work.

---

## Property Manager Page

The Property Manager Page for the flat isogrid feature is shown below:

<div class="image-annot"
     style="--image-max-width: 300px;
            --overlay-width: 500px;
            --callout-size: 22px;
            --callout-stroke: 2px;
            --callout-font-size: 6px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="/images/flat-isogrid-pmp.png" alt="Flat Isogrid Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) preview-options -->
    <a href="#preview-options" aria-label="Preview Options">
      <svg class="callout-svg" x="15" y="-23">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">1</text>
      </svg>
    </a>

    <!-- 2) face-references -->
    <a href="#face-references" aria-label="Face References">
      <svg class="callout-svg" x="15" y="-8">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">2</text>
      </svg>
    </a>

    <!-- 3) sketch-reference -->
    <a href="#sketch-reference" aria-label="Sketch Reference">
      <svg class="callout-svg" x="15" y="3">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">3</text>
      </svg>
    </a>

    <!-- 4) pattern-edge-reference -->
    <a href="#pattern-edge-reference" aria-label="Pattern Edge Reference">
      <svg class="callout-svg" x="15" y="16">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">4</text>
      </svg>
    </a>

    <!-- 5) pattern-starting-point-reference -->
    <a href="#pattern-starting-point-reference" aria-label="Pattern Starting Point Reference">
      <svg class="callout-svg" x="15" y="30">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">5</text>
      </svg>
    </a>

    <!-- 6) point-direction-offset-reference -->
    <a href="#point-direction-offset-reference" aria-label="Point Direction Offset Reference">
      <svg class="callout-svg" x="15" y="51">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">6</text>
      </svg>
    </a>

    <!-- 7) point-angle-offset-reference -->
    <a href="#point-angle-offset-reference" aria-label="Point Angle Offset Reference">
      <svg class="callout-svg" x="15" y="63">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">7</text>
      </svg>
    </a>

    <!-- 8) allow-partial-bodies -->
    <a href="#allow-partial-bodies" aria-label="Allow Partial Bodies">
      <svg class="callout-svg" x="15" y="74">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">8</text>
      </svg>
    </a>

    <!-- 9) material-thickness -->
    <a href="#material-thickness" aria-label="Material Thickness">
      <svg class="callout-svg" x="15" y="88.5">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">9</text>
      </svg>
    </a>

    <!-- 10) hole-to-hole-distance -->
    <a href="#hole-to-hole-distance" aria-label="Hole to Hole Distance">
      <svg class="callout-svg" x="15" y="103">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">10</text>
      </svg>
    </a>

    <!-- 11) parameter-definition-type -->
    <a href="#parameter-definition-type" aria-label="Parameter Definition Type">
      <svg class="callout-svg" x="15" y="121">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">11</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="preview-options"></a>1) Preview Options

There are two preview options: preview seed only and preview holes only. These are both options because for large isogrid patterns rendering the feature preview can take a long time. These options help you to adjust the isogrid parameters without having to render the whole pattern every time

Preview seed only only previews the first hole and the six surrounding triangles.

Preview holes only only previews the hole features and does not create any of the triangles. This can be good for seeing how the pattern will propogate over large distances.

No matter what preview options are selected, when the feature is committed (you hit the green check mark), the same thing will happen. The options affect the preview only

### <a id="face-references"></a>2) Face References

These face references control which faces the isogrid should pattern to. Multiple faces can be selected, but they should all be on the same plane. This can be useful for sheet metal parts where you can unfold the part, isogrid the surfaces you want to, and then refold the part.

Using one isogrid pattern instead of multiple has a few advantages. It lets you edit only one feature if you want to update the pattern. It also ensures that the same pattern is propogated across multiple faces, meaning that the hole to hole distance would remain constant

Only flat faces can be selected in this feature

By default, the center of the first selected face is used as the starting point for the isogrid pattern

### <a id="sketch-reference"></a>3) Sketch Reference

The sketch reference can serve as either a replacement or an augmentation to the face selection option. 

If a sketch is selected and no face is selected, the base plane of the sketch will be used instead of the face reference.

If a sketch and face are selected, the face will be used as the base and the sketch will be used as the bounding area. There is not much a difference either way if you select a face or not

The sketch here is used to bound the propegation of the isogrid pattern. The sketch contour will act as the edge of the face and not let the pattern go any further, or if allow partial bodies is selected it will be used to cut the partial bodies.

Multiple closed loops in the same sketch are allowed but nested loops can get a little weird sometimes. If you play with it a little you should be able to get most things to work. If you are messing with nested loops, it is important to consider where the pattern starts because that will be the loop that the isogrid is patterned within

### <a id="pattern-edge-reference"></a>4) Pattern Edge Reference

The pattern edge reference is used to direct the angle of the isogrid. The isogrid pattern will be made to be parallel to the selected edge

If this is left blank then the longest edge of the selected face will be used as the edge reference

### <a id="pattern-starting-point-reference"></a>5) Pattern Starting Point Reference

The pattern starting point is used as the point of the first hole of the isogrid pattern. 

By default it is the center of the first selected face but this lets you override that. You can use most types of SolidWorks points as this selection, but sketch points are usually easiest

### <a id="point-direction-offset-reference"></a>6) Point Direction Offset Reference

The point direction offsets allow you to toggle the starting point of the pattern with parameters instead of a point of your own. 

Offset direction 1 moves the starting point perpendicular to the pattern edge and offset direction 2 moves the point parallel to the pattern edge

These can be use to try to get a pattern to fit better on a weird face if the edges of the isogrid are falling in weird places

### <a id="point-angle-offset-reference"></a>7) Point Angle Offset Reference

The angle offset allows you to toggle the angle of the isogrid manually instead of needing to rely on a pattern edge

This can be useful when you want an isogrid pattern to go in a certain direction but there is no edge in that direction to make the pattern parallel to

### <a id="allow-partial-bodies"></a>8) Allow Partial Bodies

Typically the isogrid pattern will follow sheet metal rules, keeping all cuts 2 * material thickness away from all edges. Allow partial bodies allows you to force the pattern to cut all the way up to the edge of the face. 

### <a id="material-thickness"></a>9) Material Thickness

Material thickness is one of the main parameters of the isogrid pattern. By "Parameter Definition Type" equal to "default" (11), it controls most of the parameters of isogrid including minimum spar width, minimum distance to edge, hole diameter, arc radius, and cut depth. More information on this is under (11).

Material thickness is meant to be the thickness of the sheet that the isogrid is being patterned on, but it can also be adjusted as more of a "master parameter" to adjust the overall size of the isogrid. 

### <a id="hole-to-hole-distance"></a>10) Hole to Hole Distance

The hole to hole distance is measured by the distance from one hole to its 6 neighbors along each spar. This controls the overall size of the isgorid triangles

### <a id="parameter-definition-type"></a>11) Parameter Definition Types

Parameter definition type controls how the isogrid parameters are controlled. There are three modes: default, default + hole diameter, and define all directly. The default type is what is shown above in the itemized image. 

Default + hole diameter is meant to be used when you want the default settings but want to specify a hole diameter for maybe a certain bolt size or to tap it.

The settings for define all directly are shown below:

<p align="center">
  <img src="/images/define-all-directly-pmp.png" width="200">
</p>

Minimum spar width is the width of the spar between triangles. By default it is 2 * material thickness

Minimum distance to edge deletes all cuts that are within this distance from the edge. There is a small difference between this being set to 0 and "allow partial bodies." If this is set to zero it will allow all full cut bodies to remain but delete all partial bodies. By default this is set to 2 * material thickness

Hole to Hole distance is defined in (10)

Arc radius is the inner triangle arc radius for each triangular cut. By default it is set to material thickness

Cut depth is the depth that the cutting bodies go into the material. By default it is set to material thickness. This can be useful to cut further into a body than the default

---

## Tips and General Thoughts

1. I recommend always leaving the "preview seed only" option checked unless you know it won't take very long to render the preview. It saves a lot of time when previewing and you usually don't need to see the full pattern to get an idea of what it will look like

2. For an isogrid pattern that spans multiple faces, if you want to guarantee that the isogrid patterns are centered on each of their respective faces, then make separate isogrid patterns for each face.

3. If you give the feature a set of parameter inputs that are invalid, no preview will show and an error will be thrown if you try to create the pattern. For example, if you make the arc radius of the triangle so large that they are bigger than the triangle and start to overlap with each other, that would be an invalid geometry and no preview would be created. There are many other examples of invalid geometries.

4. The starting point only matters for what the pattern will end up looking like, it does not necessarily have to be on the face getting cut, so if part of it is hanging off the edge or over a hole or something don't worry about it.

5. If you edit a flat isogrid feature and decide that you don't actually want to change anything, x out of the property manager page instead of checking out of it, this will be much quicker as it wont recalculate all of the geometry again.

