# Cylindrical Isogrid Feature

<p align="left">
  <img src="/demo-images/iso-cyl1.png" width="225">
  <img src="/demo-images/iso-cyl2.png" width="250">
  <img src="/demo-images/iso-cyl3.png" width="175">
</p>

## Feature Overview

The cylindrical isogrid feature automatically cuts isogrid into a cylindrical surface. There are many ways this can be customized, with different sized isogrid patterns. It creates a circular pattern around the diameter of the cylinder first and then linearly copies that alone the height of the cylinder

This feature typically only works well if the cutting triangles are small enough to have around 8 triangular cuts around the diameter of the cylinder. Otherwise the triangular cuts will distort too much around the curved surface and mess up the pattern. More information on this in Tips and General Thoughts

---

## Property Manager Page

The Property Manager Page for the cylindrical isogrid feature is shown below:

<div class="image-annot"
     style="--image-max-width: 235px;
            --overlay-width: 500px;
            --callout-size: 22px;
            --callout-stroke: 2px;
            --callout-font-size: 6px;
            --callout-stroke-color: red;
            --callout-text-color: red;
            --callout-stroke-hover: blue;
            --callout-text-hover: blue;">
  <img src="/images/cylindrical-isogrid-pmp.png" alt="Flat Isogrid Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) preview-options -->
    <a href="#preview-options" aria-label="Preview Options">
      <svg class="callout-svg" x="10" y="-32">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">1</text>
      </svg>
    </a>

    <!-- 2) face-references -->
    <a href="#face-references" aria-label="Face References">
      <svg class="callout-svg" x="10" y="-18">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">2</text>
      </svg>
    </a>

    <!-- 3) sketch-reference -->
    <a href="#sketch-reference" aria-label="Sketch Reference">
      <svg class="callout-svg" x="10" y="10">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">3</text>
      </svg>
    </a>

    <!-- 4) pattern-edge-reference -->
    <a href="#pattern-edge-reference" aria-label="Pattern Edge Reference">
      <svg class="callout-svg" x="10" y="26">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">4</text>
      </svg>
    </a>

    <!-- 5) pattern-starting-point-reference -->
    <a href="#pattern-starting-point-reference" aria-label="Pattern Starting Point Reference">
      <svg class="callout-svg" x="10" y="43">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">5</text>
      </svg>
    </a>

    <!-- 6) point-direction-offset-reference -->
    <a href="#point-direction-offset-reference" aria-label="Point Direction Offset Reference">
      <svg class="callout-svg" x="10" y="60">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">6</text>
      </svg>
    </a>

    <!-- 7) point-angle-offset-reference -->
    <a href="#point-angle-offset-reference" aria-label="Point Angle Offset Reference">
      <svg class="callout-svg" x="10" y="76">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">7</text>
      </svg>
    </a>

    <!-- 8) allow-partial-bodies -->
    <a href="#allow-partial-bodies" aria-label="Allow Partial Bodies">
      <svg class="callout-svg" x="10" y="93">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">8</text>
      </svg>
    </a>

    <!-- 9) material-thickness -->
    <a href="#material-thickness" aria-label="Material Thickness">
      <svg class="callout-svg" x="10" y="110">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">9</text>
      </svg>
    </a>

    <!-- 10) hole-to-hole-distance -->
    <a href="#hole-to-hole-distance" aria-label="Hole to Hole Distance">
      <svg class="callout-svg" x="10" y="128">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">10</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="preview-options"></a>1) Isogrid Face References

The cylindrical face that the isogrid should go on. It does not need to be a complete cylinder, it can be some kind of partial cylinder

Once this face is selected, the part body is hidden so you can see the isogrid pattern more clearly

### <a id="face-references"></a>2) Preview Options

There are three preview options avaliable for this feature. 

No preview means that no preview will be shown before the feature is created

Preview Seed Only will show the preview for two of the triangles and the holes around them.

Preview First Row Only will preview the first row around the cylinder but now the linear pattern along the cylinder

### <a id="sketch-reference"></a>3) Estimated Spar Width

Minimum spar width provides a rough minimum distance for all of the spars between cuts. This number is more of an approximation than an exact number. This is because all the cuts are created as lofts to a point located on the axis of the cylinder, and this causes the distances between the cuts to change as they get closer to the center of the cylinder

### <a id="pattern-edge-reference"></a>4) Minimum Distance to Edge

This is used to prevent cuts being too close to an edge if "Check cuts too close to edges" (9) is selected. Any cut closer than this distance will not be cut. 

The way these cut distances are check is by making a mesh of points around each cut and then checking the distance from these points to each edge of the cylindrical face. The resolution of this mesh can be set by "Check Edge Mesh Options (10). Rough should be fine for most cylindrical isogrids but if you are extra worried about making sure cuts are far enough away from edge you can change this value.

### <a id="pattern-starting-point-reference"></a>5) Hole to Hole Distance

This is the rough hole to hole distance for each hole cut to its six adjacent hole cuts. 

This value is rounded behind the scenes to the nearest hole to hole distance that allows for the cuts to pattern around the cylinder. Because the pattern needs to line up around the circular direction of the cylidner, there are only select values that will pattern so that the pattern is continuous. This is why small changes in this value will likely not affect the overall cylindrical isogrid pattern

### <a id="point-direction-offset-reference"></a>6) Hole Diameter

Hole diameter is an approximate value for the diameter of the cutting holes. This is only an approximate value because the diameter will change as the loft goes closer to the center axis of the cylinder

### <a id="point-angle-offset-reference"></a>7) Arc Radius

Arc radius is an approximate value for the inner radius of the cutting triangles. This is only an approximate value because the radius will change as the cutting loft goes closer to the center axis of the cylinder

### <a id="allow-partial-bodies"></a>8) Cut Depth

Cut depth is how far each cutting body will cut radially into the cylinder

### <a id="material-thickness"></a>9) Check for Cuts Close to Edge

Check for cuts close to edge enables "Minimum Distance to Edge" (4) to ensure that all cutting bodies are a certain distance from all edges of the face

### <a id="hole-to-hole-distance"></a>10) Check Edge Mesh Refinement Options

This controls how detailed "Minimum Distance to Edge" (4) should be when checking to make sure that all cuts are a certain distance from each edge

You should pretty much always just leave this on "Rough" and not worry about it, but I wanted to give an option for higher resolution in case anyone wanted it

---

## Tips and General Thoughts

1. Cylindrical isogrid is made by creating flat filleted triangles and circles and lofting them towards a point on the axis of the cylinder. In a perfect world they would be lofted to a line instead of a point, but that ended up not working consistantly so they loft to a point instead. This lofting has two main effects, talked about in points 2 and 3.

2. The first effect of lofting is that the edges of the cuts get distorted if the filleted triangular cuts go around too much of the cylinder curve. This feature accounts for small amounts of this curved distortion fine, but if the cuts become too relativly large (around more than 8 cuts around the circumference) the pattern will become distorted strangely. This can be overcome with some amount of manual editing outside of this feautre, but the feature will not work by default

3. The second effect of lofting is that as you get closer to the center axis of the cylinder, the cuts become more spaced out. This becomes important for very deep cuts or if you are using cylindrical isogrid bodies to cut another non-perfect cylinder surface (more info on this below)

4. You can use this feature to create cylindrical isogrid bodies to cut other parts. To do this, create a cylinder a little larger than the surface you want to add isogrid to. Add cylindrical isogrid to this and make the cut depth go as far into the cylinder as needed. Making it cut all the way to the axis can have some weird effects so I recomend adding some buffer there to end the cut depth before it gets all the way to the center. Then create another cylinder with a hair smaller diameter than the first one (to let you select both bodies). Using direct editing "combine", select subtract, select the second cylinder as the main body, and select the isogrid pattern as the "bodies to combine." Click the check mark and you should be left with cylindrical isogrid cutting bodies. You can do another direct edit combine subtraction to remove these bodies from the surface you wanted to isogrid

5. Because of the way the lofting is done, there are no radial overhangs in the isogrid, which should make it easier to machine. This is true of all the curved isogrid patterns

