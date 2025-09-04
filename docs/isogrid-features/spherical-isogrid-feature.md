# Spherical Isogrid Feature

<p align="left">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/iso-sphere1.png" width="225">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/iso-sphere2.png" width="225">
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/demo-images/iso-sphere3.png" width="225">
</p>

## Feature Overview

The spherical isogrid feature automatically cuts isogrid into a spherical surface. There are many ways this can be customized, with different sized isogrid patterns, and different numbers of cuts. It works by following a geodesic sphere based on an icosahedron

Unlike the other types of isogrid, spherical needs to pattern in multiple curved directions, limiting the number of patterns that can pattern correctly. This is why it is based around a geodesic sphere with different levels of detail.

---

## Property Manager Page

The Property Manager Page for the spherical isogrid feature is shown below:

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
  <img src="https://tamu-edu.github.io/rad_lab_rad_cad_documentation/images/spherical-isogrid-pmp.png" alt="Flat Isogrid Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) preview-options -->
    <a href="#preview-options" aria-label="Preview Options">
      <svg class="callout-svg" x="10" y="-50">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">1</text>
      </svg>
    </a>

    <!-- 2) face-references -->
    <a href="#face-references" aria-label="Face References">
      <svg class="callout-svg" x="10" y="-40">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">2</text>
      </svg>
    </a>

    <!-- 3) sketch-reference -->
    <a href="#sketch-reference" aria-label="Sketch Reference">
      <svg class="callout-svg" x="10" y="-28">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">3</text>
      </svg>
    </a>

    <!-- 4) pattern-edge-reference -->
    <a href="#pattern-edge-reference" aria-label="Pattern Edge Reference">
      <svg class="callout-svg" x="10" y="-6">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">4</text>
      </svg>
    </a>

    <!-- 5) pattern-starting-point-reference -->
    <a href="#pattern-starting-point-reference" aria-label="Pattern Starting Point Reference">
      <svg class="callout-svg" x="10" y="8">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">5</text>
      </svg>
    </a>

    <!-- 6) point-direction-offset-reference -->
    <a href="#point-direction-offset-reference" aria-label="Point Direction Offset Reference">
      <svg class="callout-svg" x="10" y="24">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">6</text>
      </svg>
    </a>

    <!-- 7) point-angle-offset-reference -->
    <a href="#point-angle-offset-reference" aria-label="Point Angle Offset Reference">
      <svg class="callout-svg" x="10" y="40">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">7</text>
      </svg>
    </a>

    <!-- 8) allow-partial-bodies -->
    <a href="#allow-partial-bodies" aria-label="Allow Partial Bodies">
      <svg class="callout-svg" x="10" y="57">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">8</text>
      </svg>
    </a>

    <!-- 9) material-thickness -->
    <a href="#material-thickness" aria-label="Material Thickness">
      <svg class="callout-svg" x="10" y="73">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="3.5"></circle>
        <text x="11" y="11.75">9</text>
      </svg>
    </a>

    <!-- 10) hole-to-hole-distance -->
    <a href="#hole-to-hole-distance" aria-label="Hole to Hole Distance">
      <svg class="callout-svg" x="10" y="91">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">10</text>
      </svg>
    </a>

    <!-- 11) parameter-definition-type -->
    <a href="#parameter-definition-type" aria-label="Parameter Definition Type">
      <svg class="callout-svg" x="10" y="107">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">11</text>
      </svg>
    </a>

    <!-- 11) parameter-definition-type -->
    <a href="#inside-face" aria-label="Parameter Definition Type">
      <svg class="callout-svg" x="10" y="121">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">12</text>
      </svg>
    </a>

    <!-- 11) parameter-definition-type -->
    <a href="#edge-mesh-refinement-options" aria-label="Parameter Definition Type">
      <svg class="callout-svg" x="10" y="140">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="11.75">13</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="preview-options"></a>1) Isogrid Face References

The spherical face that the isogrid should go on. It does not need to be a complete sphere, it can be some kind of partial sphere or dome, as long as the surface has a constant radius. Only one face can be selected

Once this face is selected, the part body is hidden so you can see the isogrid pattern more clearly

### <a id="face-references"></a>2) Pattern Edge Reference

This is meant to be a reference axis that the spherical isogrid should be patterned about. By default, the pattern will have two mirroring holes along the x axis, but if you want the pattern to created about a different axis you can use this reference to change that default.

The location of this axis does not matter, only its direction

### <a id="sketch-reference"></a>3) Preview Options

There are four preview options avaliable for this feature. "Create Loft Bodies Only" does more than just change the preview and you can read more about that below in section 4.  

No preview means that no preview will be shown before the feature is created. Sometimes if no preview is selected on creation it will throw an error. If you are getting errors and are not sure why try unchecking this box

Preview Seed Only will show the preview for one of the original triangles and the holes around. If number of layers to pattern goes up, it will also show the sub triangles and holes inside that original triangle. If preview holes only is also selected, this option will only show the three cutting holes

Preview Holes Only will only show the holes across the entire feature. This can be a good idea to see how the isogrid will propogate without having to render every triangular body, especially as "number of layers to pattern" increases.

Create Loft Bodies Only is talked about more below. For this feature what is shown in preview is also what will be generated

### <a id="pattern-edge-reference"></a>4) Create Loft Bodies

Create Loft Bodies creates the cutting bodies for the spherical isogrid instead of cutting them into the sphere. This is mean to be used to cut bodies that are not perfectly spherical

For examply, if you want to isogrid an ellipsoid: Make a sphere larger than the ellipsoid and add spherical isogrid to it. Use this "Create Loft Bodies" option to create the loft bodies for the isogrid. The use direct editing to subtract the loft bodies from the ellipsoid.

### <a id="pattern-starting-point-reference"></a>5) Number of Layers to Pattern

Number of Layers to Pattern determines how many triangular cuts are made into the sphere. Since spherical isogrid start with an isohedron as a base, a layer pattern number of 1 means there will be 20 triangular cuts. Each layer beyond that splits each original triangle into four triangles.

Because the number of triangles grows so quickly, it is extremely advisable not to push this number past 3.

### <a id="point-direction-offset-reference"></a>6) Minimum Spar Width

Minimum spar width provides a rough minimum distance for all of the spars between cuts. This number is more of an approximation than an exact number. This is because all the cuts are created as lofts to a point at the center of the sphere, and this causes the distances between the cuts to change as they get closer to the center of the sphere

### <a id="point-angle-offset-reference"></a>7) Minimum Distance to Edge

This is used to prevent cuts being too close to an edge if "Delete cuts too close to edges" (11) is selected. Any cut closer than this distance will not be cut. 

The way these cut distances are check is by making a mesh of points around each cut and then checking the distance from these points to each edge of the spherical face. The resolution of this mesh can be set by "Check Edge Mesh Refinement Options (13). Rough should be fine for most spherical isogrids but if you are extra worried about making sure cuts are far enough away from edge you can change this value.

This value cannot be too close to 0 or an error will occur

### <a id="allow-partial-bodies"></a>8) Hole Diameter

Hole diameter is an approximate value for the diameter of the cutting holes. This is only an approximate value because the diameter will change as the loft goes closer to the center of the sphere

### <a id="material-thickness"></a>9) Arc Radius

Arc radius is an approximate value for the inner radius of the cutting triangles. This is only an approximate value because the radius will change as the cutting loft goes closer to the center of the sphere

### <a id="hole-to-hole-distance"></a>10) Cut Depth

Cut depth is how far each cutting body will cut radially into the sphere

### <a id="parameter-definition-type"></a>11) Check for Cuts Close to Edge

Check for cuts close to edge enables "Minimum Distance to Edge" (7) to ensure that all cutting bodies are a certain distance from all edges of the face

Additionally, be careful when cutting onto a sphere because the "seam" left behind from a revolve will count as an edge when checking for edges sometimes.

### <a id="inside-face"></a>12) Inside Face

Inside face, if enabled, will make the spherical isogrid cut outwards from the face instead of in towards the face. It should be used if the spherical face is an inner face instead of an outer face

### <a id="edge-mesh-refinement-options"></a>13) Check Edge Mesh Refinement Options

This controls how detailed "Minimum Distance to Edge" should be when checking to make sure that all cuts are a certain distance from each edge

You should pretty much always just leave this on "Rough" and not worry about it, but I wanted to give an option for higher resolution in case anyone wanted it


---

## Tips and General Thoughts

1. As mentioned in "Create Loft Bodies" (4), this can be used for more than just spherical surfaces. This Can be used for most concave surfaces you want to add isogrid to that follow a roughly spherical curvature.

2. When using spherical isogrid on a perfect sphere, no edge distance checking will be done

3. This feature works by creating flat filleted triangles and circles off the surface of the sphere and the lofting those regions towards the center of the sphere. This can be helpful to understand why some of the parameters are not exact values

4. Because of the way the lofting is done, there are no radial overhangs in the isogrid, which should make it easier to machine. This is true of all the curved isogrid patterns

