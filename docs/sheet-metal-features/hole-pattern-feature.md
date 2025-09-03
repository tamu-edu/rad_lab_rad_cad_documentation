# Hole Pattern Feature

<p align="left">
<img src="/demo-images/hole1.png" width="225">
  <img src="/demo-images/hole2.png" width="225">
  <img src="/demo-images/hole3.png" width="225">
</p>

## Feature Overview

The hole pattern feature allows you to make hole patterns on the edges of sheet metal parts. This is most useful for creating rivet holes to attach two sheet metal parts together. There are many different types of hole patterns avaliable within this feature

---

## Property Manager Page

The Property Manager Page for the hole pattern feature is shown below:

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
  <img src="/images/hole-pattern-pmp.png" alt="Hole Pattern Property Manager Page">

  <!-- Scalable overlay aligned to the image -->
  <svg viewBox="0 0 120 110" preserveAspectRatio="xMidYMid meet" aria-hidden="true">

    <!-- 1) Hole Pattern Face -->
    <a href="#param-1" aria-label="Hole Pattern Face">
      <svg class="callout-svg" x="12" y="-7">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">1</text>
      </svg>
    </a>

    <!-- 2) Hole Pattern Edge -->
    <a href="#param-2" aria-label="Hole Pattern Edge">
      <svg class="callout-svg" x="12" y="7">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">2</text>
      </svg>
    </a>

    <!-- 3) Material Thickness -->
    <a href="#param-3" aria-label="Material Thickness">
      <svg class="callout-svg" x="12" y="22">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">3</text>
      </svg>
    </a>

    <!-- 4) Hole Number Offset -->
    <a href="#param-4" aria-label="Hole Number Offset">
      <svg class="callout-svg" x="12" y="32">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">4</text>
      </svg>
    </a>

    <!-- 5) Cut Edge to Face Edge Distance -->
    <a href="#param-5" aria-label="Cut Edge to Face Edge Distance">
      <svg class="callout-svg" x="12" y="44">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">5</text>
      </svg>
    </a>

    <!-- 6) Vertical Hole Edge Distance -->
    <a href="#param-6" aria-label="Vertical Hole Edge Distance">
      <svg class="callout-svg" x="12" y="53">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">6</text>
      </svg>
    </a>

    <!-- 7) Horizontal Hole Edge Distance -->
    <a href="#param-7" aria-label="Horizontal Hole Edge Distance">
      <svg class="callout-svg" x="12" y="62">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">7</text>
      </svg>
    </a>

    <!-- 8) Cut Depth -->
    <a href="#param-8" aria-label="Cut Depth">
      <svg class="callout-svg" x="12" y="71">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">8</text>
      </svg>
    </a>

    <!-- 9) Powder Coat Offset -->
    <a href="#param-9" aria-label="Powder Coat Offset">
      <svg class="callout-svg" x="12" y="80">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">9</text>
      </svg>
    </a>

    <!-- 10) Hole Pattern Type -->
    <a href="#param-10" aria-label="Hole Pattern Type">
      <svg class="callout-svg" x="12" y="91">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">10</text>
      </svg>
    </a>

    <!-- 11) Hole Diameter Type -->
    <a href="#param-11" aria-label="Hole Diameter Type">
      <svg class="callout-svg" x="12" y="103">
        <rect class="hit" width="100%" height="100%" fill="transparent"></rect>
        <circle cx="11" cy="11" r="4"></circle>
        <text x="11" y="12">11</text>
      </svg>
    </a>

  </svg>
</div>

---

## Parameters

### <a id="param-1"></a>1) Hole Pattern Face

This is the face that the hole pattern will be added to. It is the face that the holes will be cut into

### <a id="param-2"></a>2) Hole Pattern Edge

This is the edge that will be used as a reference for creating the hole pattern. The pattern will be close to this edge and will also use the length of this edge to determine how far to extend the hole pattern. The hole pattern will start at the center of this edge

### <a id="param-3"></a>3) Hole Pattern Variables — Material Thickness

Material thickness is used as a sort of "master parameter" that controls most of the advanced variables (5-8) on its own. This is what is used to determine how far the hole pattern should go and where it should be. The general rule for sheet metal is that all cuts should be made at least 2 * material thickness from the edge. For the hole pattern this is extended to also mean that the holes are at least 2 * material thickness from each other. Finally the hole pattern is cut into the material the same depth as the material thickness.

If you update material thickness the advanced variables will all update accordingly, but you can edit any one of the advanced variables individually and the rest will remain the same

### <a id="param-4"></a>4) Hole Pattern Variables — Hole Number Offset

Hole number offset acts as a way of telling the hole pattern to cut more or less holes into the sheet. 

A positive value will tell the pattern to make one more row of holes along the edge. Be careful though because this will allow you to violate the sheet metal rules about keeping holes far enough away from the edge

A negative value will tell the pattern to make one fewer row of holes along the edge. This can be useful if you do not want the hole pattern to extend all the way to the edge

### <a id="param-5"></a>5) Advanced Variables — Cut Edge to Face Edge Distance

This is the distance from the outer edge of the cutting hole to the edge of the face. It is 2 * material thickness by default

### <a id="param-6"></a>6) Advanced Variables — Vertical Hole Edge Distance

This is the distance of the holes from cutting edge to cutting edge perpendicular to the length of the edge. It is 2 * material thickness by default

### <a id="param-7"></a>7) Advanced Variables — Horizontal Hole Edge Distance

This is the distance of the holes from cutting edge to cutting edge along the length of the edge. It is 2 * material thickness by default

### <a id="param-8"></a>8) Advanced Variables — Cut Depth

This is the depth that the hole pattern cuts into the material. It is material thickness by default

### <a id="param-9"></a>9) Advanced Variables — Powder Coat Offset

Powder coating a sheet metal part adds a little bit of thickness to the inside of the hole pattern. If you want to avoid drilling out every hole, this can be a useful way to account for that additional thickness. It adds 0.01 inches to the diameter of every hole

### <a id="param-10"></a>10) Hole Pattern Type

There are several different hole pattern options in this feature. The different options are shown below. The differences between "checker pattern 1" and "checker pattern 2" is which hole starts at the center. The same difference is true for "domino pattern 1" and "domino pattern 2"

<p align="center">
  <img src="/images/hole-pattern-types.png" width="725">
</p>

### <a id="param-11"></a>11) Hole Diameter Type

Hole diameter type allows you to determine how to set the diameter of the hole. One option is to define the hole diameter directly using the input box below this drop down menu. The other is to select one of the rivet presets from this drop down menu. 

The rivet hole sizes are determined according to the McMaster-Carr recomended hole diameter sizes for [Aluminum Domed Head Blind Rivets]("https://www.mcmaster.com/products/rivets/rivets-2~/aluminum-domed-head-blind-rivets/"). If you are using a different rivet type you should use the define hole diameter directly option

If you select the hole diameter according to a rivet type, the rivet feature will automatically detect your selection and match the rivets according to what type was selected in this hole pattern feature

Adding a powder coat offset will work the same regardless of hole diameter type

---

## Tips and General Thoughts

1. Hole pattern assumes the the edge you are using as an edge reference is perpendicular to the other two edges connected to it. Essentially it assumes you are hole patterning on the edge of a rectangle. This is the assumption it uses to calculate how many holes to make in the pattern and how far the pattern should extend before it gets closer than 2 * material thickness to an edge. If you are hole patterning an edge that does not fit this assumption, you might need to manually make sure a hole does not get cut too close to an edge.

2. If you are trying to get two part's hole patterns to line up in an assembly so you can put rivets through them, you should hole pattern one part and use cross drill on the other part to guarantee that they line up correctly. More on this in the cross drill documentation

3. The automatic spacing for hole patterns is to have two times material thickness between each hole. However, based on your material thickness, rivet type, and pattern type, this may be too close together for every rivet to fit. You should use the rivet feature to ensure that the spacing is fine and adjust paramters accordingly