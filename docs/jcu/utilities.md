---
layout: docs
title: Utility classes
group: jcu
---

This framework includes various utilities—classes with a single purpose. They're
designed to reduce the frequency of highly repetitive declarations in your CSS
down while allowing for quick and easy development.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Opacity control

Configure the opacity of a given element.  This is styled in such a way that
browsers can animate the property when its value changes.

* `.opaque`: make an element fully visible with `opacity: 1`
* `.transparent`: make an element invisible with `opacity: 0`

## Borders

This small utility follows on the [spacing
utilities]({{ site.baseurl }}/components/utilities/#spacing) provided by the
core framework.

* `.b-a-0`: configure all borders (indicated by the `b-a`) to be none (indicated
  the `0`)

## Backgrounds

You can use any of the following colours and opacities and mix them into any
other block elements to provide a coloured semi-transparent background.

{% callout warning %}
#### Conveying meaning to assistive technologies

Ensure that any meaning conveyed through color is also conveyed in a format that
is not purely presentational.
{% endcallout %}

For details on dealing with selector specificity, refer the [Contextual Colors
and Backgrounds](
{{ site.baseurl }}/components/utilities/#contextual-colors-and-backgrounds)
documentation from Bootstrap.

### Complete palette

<div class="row jcu-bg-examples jcu-bg--green-leaf-swirl">
  <div class="col-xs-3">
    <div class="jcu-bg--pink-25pc">.jcu-bg--pink-25pc</div>
    <div class="jcu-bg--pink-50pc">.jcu-bg--pink-50pc</div>
    <div class="jcu-bg--pink-75pc">.jcu-bg--pink-75pc</div>
    <div class="jcu-bg--pink-90pc">.jcu-bg--pink-90pc</div>
    <div class="jcu-bg--pink">.jcu-bg--pink</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--red-25pc">.jcu-bg--red-25pc</div>
    <div class="jcu-bg--red-50pc">.jcu-bg--red-50pc</div>
    <div class="jcu-bg--red-75pc">.jcu-bg--red-75pc</div>
    <div class="jcu-bg--red-90pc">.jcu-bg--red-90pc</div>
    <div class="jcu-bg--red">.jcu-bg--red</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--red-dark-25pc">.jcu-bg--red-dark-25pc</div>
    <div class="jcu-bg--red-dark-50pc">.jcu-bg--red-dark-50pc</div>
    <div class="jcu-bg--red-dark-75pc">.jcu-bg--red-dark-75pc</div>
    <div class="jcu-bg--red-dark-90pc">.jcu-bg--red-dark-90pc</div>
    <div class="jcu-bg--red-dark">.jcu-bg--red-dark</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--orange-25pc">.jcu-bg---orange-25pc</div>
    <div class="jcu-bg--orange-50pc">.jcu-bg---orange-50pc</div>
    <div class="jcu-bg--orange-75pc">.jcu-bg---orange-75pc</div>
    <div class="jcu-bg--orange-90pc">.jcu-bg---orange-90pc</div>
    <div class="jcu-bg--orange">.jcu-bg---orange</div>
  </div>
  <div class="clearfix hidden-sm-up"></div>
  <div class="col-xs-3">
    <div class="jcu-bg--yellow-25pc">.jcu-bg---yellow-25pc</div>
    <div class="jcu-bg--yellow-50pc">.jcu-bg--yellow-50pc</div>
    <div class="jcu-bg--yellow-75pc">.jcu-bg--yellow-75pc</div>
    <div class="jcu-bg--yellow-90pc">.jcu-bg--yellow-90pc</div>
    <div class="jcu-bg--yellow">.jcu-bg--yellow</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--green-light-25pc">.jcu-bg--green-light-25pc</div>
    <div class="jcu-bg--green-light-50pc">.jcu-bg--green-light-50pc</div>
    <div class="jcu-bg--green-light-75pc">.jcu-bg--green-light-75pc</div>
    <div class="jcu-bg--green-light-90pc">.jcu-bg--green-light-90pc</div>
    <div class="jcu-bg--green-light">.jcu-bg--green-light</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--green-25pc">.jcu-bg--green-25pc</div>
    <div class="jcu-bg--green-50pc">.jcu-bg--green-50pc</div>
    <div class="jcu-bg--green-75pc">.jcu-bg--green-75pc</div>
    <div class="jcu-bg--green-90pc">.jcu-bg--green-90pc</div>
    <div class="jcu-bg--green">.jcu-bg--green</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--blue-light-25pc">.jcu-bg--blue-light-25pc</div>
    <div class="jcu-bg--blue-light-50pc">.jcu-bg--blue-light-50pc</div>
    <div class="jcu-bg--blue-light-75pc">.jcu-bg--blue-light-75pc</div>
    <div class="jcu-bg--blue-light-90pc">.jcu-bg--blue-light-90pc</div>
    <div class="jcu-bg--blue-light">.jcu-bg--blue-light</div>
  </div>
  <div class="clearfix hidden-sm-up"></div>
  <div class="col-xs-3">
    <div class="jcu-bg--blue-25pc">.jcu-bg--blue-25pc</div>
    <div class="jcu-bg--blue-50pc">.jcu-bg--blue-50pc</div>
    <div class="jcu-bg--blue-75pc">.jcu-bg--blue-75pc</div>
    <div class="jcu-bg--blue-90pc">.jcu-bg--blue-90pc</div>
    <div class="jcu-bg--blue">.jcu-bg--blue</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--blue-dark-25pc">.jcu-bg--blue-dark-25pc</div>
    <div class="jcu-bg--blue-dark-50pc">.jcu-bg--blue-dark-50pc</div>
    <div class="jcu-bg--blue-dark-75pc">.jcu-bg--blue-dark-75pc</div>
    <div class="jcu-bg--blue-dark-90pc">.jcu-bg--blue-dark-90pc</div>
    <div class="jcu-bg--blue-dark">.jcu-bg--blue-dark</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--black-25pc">.jcu-bg--black-25pc</div>
    <div class="jcu-bg--black-50pc">.jcu-bg--black-50pc</div>
    <div class="jcu-bg--black-75pc">.jcu-bg--black-75pc</div>
    <div class="jcu-bg--black-90pc">.jcu-bg--black-90pc</div>
    <div class="jcu-bg--black">.jcu-bg--black</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--gray-25pc">.jcu-bg--gray-25pc</div>
    <div class="jcu-bg--gray-50pc">.jcu-bg--gray-50pc</div>
    <div class="jcu-bg--gray-75pc">.jcu-bg--gray-75pc</div>
    <div class="jcu-bg--gray-90pc">.jcu-bg--gray-90pc</div>
    <div class="jcu-bg--gray">.jcu-bg--gray</div>
  </div>
  <div class="clearfix hidden-sm-up"></div>
  <div class="col-xs-3">
    <div class="jcu-bg--gray-light-25pc">.jcu-bg--gray-light-25pc</div>
    <div class="jcu-bg--gray-light-50pc">.jcu-bg--gray-light-50pc</div>
    <div class="jcu-bg--gray-light-75pc">.jcu-bg--gray-light-75pc</div>
    <div class="jcu-bg--gray-light-90pc">.jcu-bg--gray-light-90pc</div>
    <div class="jcu-bg--gray-light">.jcu-bg--gray-light</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--gray-lighter-25pc">.jcu-bg--gray-lighter-25pc</div>
    <div class="jcu-bg--gray-lighter-50pc">.jcu-bg--gray-lighter-50pc</div>
    <div class="jcu-bg--gray-lighter-75pc">.jcu-bg--gray-lighter-75pc</div>
    <div class="jcu-bg--gray-lighter-90pc">.jcu-bg--gray-lighter-90pc</div>
    <div class="jcu-bg--gray-lighter">.jcu-bg--gray-lighter</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--white-25pc">.jcu-bg--white-25pc</div>
    <div class="jcu-bg--white-50pc">.jcu-bg--white-50pc</div>
    <div class="jcu-bg--white-75pc">.jcu-bg--white-75pc</div>
    <div class="jcu-bg--white-90pc">.jcu-bg--white-90pc</div>
    <div class="jcu-bg--white">.jcu-bg--white</div>
  </div>
  <div class="col-xs-3">
    <div class="jcu-bg--transparent">.jcu-bg--transparent</div>
  </div>
</div>

### Gradients

<div class="jcu-bg-examples jcu-bg-examples--inverse">
  <div class="jcu-bg--gradient-blue">.jcu-bg--gradient-blue</div>
  <div class="jcu-bg--gradient-blue-rev">.jcu-bg--gradient-blue-rev</div>
  <div class="jcu-bg--gradient-orange">.jcu-bg--gradient-orange</div>
  <div class="jcu-bg--gradient-orange-rev">.jcu-bg--gradient-orange-rev</div>
  <div class="jcu-bg--gradient-green">.jcu-bg--gradient-green</div>
  <div class="jcu-bg--gradient-green-rev">.jcu-bg--gradient-green-rev</div>
  <div class="jcu-bg--gradient-red">.jcu-bg--gradient-red</div>
  <div class="jcu-bg--gradient-red-rev">.jcu-bg--gradient-red-rev</div>
</div>

<div class="row jcu-bg-examples jcu-bg-examples--inverse">
  <div class="col-md-3 jcu-bg--gradient-blue-45deg">.jcu-bg--gradient-blue-45deg</div>
  <div class="col-sm-3 jcu-bg--gradient-orange-45deg">.jcu-bg--gradient-orange-45deg</div>
  <div class="col-sm-3 jcu-bg--gradient-green-45deg">.jcu-bg--gradient-green-45deg</div>
  <div class="col-sm-3 jcu-bg--gradient-red-45deg">.jcu-bg--gradient-red-45deg</div>
</div>

### Images

There are a number of approved brand images that can be used as backgrounds as
well.

<div class="jcu-bg-examples jcu-bg-examples--expanding jcu-bg-examples--inverse">
  <div class="jcu-bg--blue-buildings">.jcu-bg--blue-buildings</div>
  <div class="jcu-bg--blue-fish">.jcu-bg--blue-fish</div>
  <div class="jcu-bg--blue-globe">.jcu-bg--blue-globe</div>
  <div class="jcu-bg--blue-purple-fibre-optic">.jcu-bg--blue-purple-fibre-optic</div>
  <div class="jcu-bg--blue-skyscraper">.jcu-bg--blue-skyscraper</div>
  <div class="jcu-bg--fossil">.jcu-bg--fossil</div>
  <div class="jcu-bg--brown-green-yellow-grass">.jcu-bg--brown-green-yellow-grass</div>
  <div class="jcu-bg--brown-outback-road">.jcu-bg--brown-outback-road</div>
  <div class="jcu-bg--didgeridoo">.jcu-bg--didgeridoo</div>
  <div class="jcu-bg--eucalyptus-flower">.jcu-bg--eucalyptus-flower</div>
  <div class="jcu-bg--green-fern">.jcu-bg--green-fern</div>
  <div class="jcu-bg--green-grass">.jcu-bg--green-grass</div>
  <div class="jcu-bg--green-leaf-swirl">.jcu-bg--green-leaf-swirl</div>
  <div class="jcu-bg--green-rainforest">.jcu-bg--green-rainforest</div>
  <div class="jcu-bg--green-outback">.jcu-bg--green-outback</div>
  <div class="jcu-bg--green-yellow-fibre-optic">.jcu-bg--green-yellow-fibre-optic</div>
  <div class="jcu-bg--iot-circuit-board">.jcu-bg--iot-circuit-board</div>
  <div class="jcu-bg--jigsaw">.jcu-bg--jigsaw</div>
  <div class="jcu-bg--law-books">.jcu-bg--law-books</div>
  <div class="jcu-bg--multicolor-fibre-optic">.jcu-bg--multicolor-fibre-optic</div>
  <div class="jcu-bg--multicolor-fabric">.jcu-bg--multicolor-fabric</div>
  <div class="jcu-bg--orange-flower">.jcu-bg--orange-flower</div>
  <div class="jcu-bg--pink-sunset">.jcu-bg--pink-sunset</div>
  <div class="jcu-bg--pink-waterdrops">.jcu-bg--pink-waterdrops</div>
  <div class="jcu-bg--rv-james-kirby">.jcu-bg--rv-james-kirby</div>
  <div class="jcu-bg--red-blood-cells">.jcu-bg--red-blood-cells</div>
  <div class="jcu-bg--red-fibre-optic">.jcu-bg--red-fibre-optic</div>
  <div class="jcu-bg--red-flower">.jcu-bg--red-flower</div>
  <div class="jcu-bg--red-sand">.jcu-bg--red-sand</div>
  <div class="jcu-bg--silver-gears">.jcu-bg--silver-gears</div>
  <div class="jcu-bg--sunset-windmill">.jcu-bg--sunset-windmill</div>
  <div class="jcu-bg--tropics-map">.jcu-bg--tropics-map</div>
  <div class="jcu-bg--turtle-and-reef">.jcu-bg--turtle-and-reef</div>
  <div class="jcu-bg--vet-horses">.jcu-bg--vet-horses</div>
  <div class="jcu-bg--yellow-savannah">.jcu-bg--yellow-savannah</div>
  <div class="jcu-bg--yellow-shell">.jcu-bg--yellow-shell</div>
  <div class="jcu-bg--yellow-sunflower">.jcu-bg--yellow-sunflower</div>
</div>

#### Covers

Use `.jcu-bg--cover` to configure an image background to scale as large as
possible, whilst maintaining the aspect ratio, *covering* the entire width or
height of the container.  Compare the two different examples below and note how
the cover example resizes the image and may clip the edges to maintain aspect
ratio.

<div class="jcu-bg-examples jcu-bg-examples--inverse">
  <div class="jcu-bg--blue-fish jcu-bg--cover" style="height: 10em">.jcu-bg--blue-buildings .jcu-bg--cover</div>
  <hr>
  <div class="jcu-bg--blue-fish" style="height: 10em">.jcu-bg--blue-buildings (no cover class)</div>
</div>
