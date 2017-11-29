---
layout: docs
title: Navs
group: jcu
---

Navigation component customisations that are built upon the standard
[Navs]({{ site.baseurl }}/components/navs) from the core of Bootstrap.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Inverse Tabs

This is a simple example that applies the dark styling to the tabs component.
The `.nav-dark` sets the colour of the elements and `.bg-inverse` configures the
specific background colour.  The latter is adjustable

{% example html %}
<ul class="nav nav-tabs nav-dark bg-inverse">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Another link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link disabled" href="#">Disabled</a>
  </li>
</ul>
{% endexample %}

## Inverse tabs with dropdowns

{% example html %}
<ul class="nav nav-tabs nav-dark bg-inverse">
  <li class="nav-item">
    <a class="nav-link active" href="#">Active</a>
  </li>
  <li class="nav-item dropdown">
    <a class="nav-link dropdown-toggle" data-toggle="dropdown" href="#" role="button" aria-haspopup="true" aria-expanded="false">Dropdown</a>
    <div class="dropdown-menu">
      <a class="dropdown-item" href="#">Action</a>
      <a class="dropdown-item" href="#">Another action</a>
      <a class="dropdown-item" href="#">Something else here</a>
      <div class="dropdown-divider"></div>
      <a class="dropdown-item" href="#">Separated link</a>
    </div>
  </li>
  <li class="nav-item">
    <a class="nav-link" href="#">Another link</a>
  </li>
  <li class="nav-item">
    <a class="nav-link disabled" href="#">Disabled</a>
  </li>
</ul>
{% endexample %}

## Inverse interactive tabs

Use the tab JavaScript plugin—include it individually or through the compiled `bootstrap.js` file—to extend our navigational tabs and pills to create tabbable panes of local content, even via dropdown menus.

<div role="tabpanel">
  <ul class="nav nav-tabs nav-dark bg-inverse" id="inverse-tabs" role="tablist">
    <li class="nav-item">
      <a class="nav-link active" id="home-tab" data-toggle="tab" href="#home" role="tab" aria-controls="home" aria-expanded="true">Home</a>
    </li>
    <li class="nav-item">
      <a class="nav-link" id="profile-tab" data-toggle="tab" href="#profile" role="tab" aria-controls="profile">Profile</a>
    </li>
    <li class="nav-item dropdown">
      <a class="nav-link dropdown-toggle" href="#" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">
        Dropdown
      </a>
      <div class="dropdown-menu">
        <a class="dropdown-item" id="dropdown1-tab" data-toggle="tab" href="#dropdown1" role="tab" aria-controls="dropdown1">Staff</a>
        <a class="dropdown-item" id="dropdown2-tab" data-toggle="tab" href="#dropdown2" role="tab" aria-controls="dropdown2">Students</a>
      </div>
    </li>
  </ul>
  <div class="tab-content jcu-bg--gray-lighter" id="myTabContent">
    <div class="tab-pane fade in active" id="home" role="tabpanel" aria-labelledBy="home-tab">
      <h2>Main tab</h2>
      <p>Our students come from many backgrounds, promoting a rich cultural and
      experiential diversity on campus. Our undergraduate and postgraduate courses
      span the Arts, Biomedical Sciences, Business, Creative Media, Dentistry,
      Education, Engineering, Healthcare Sciences, Information Technology, Law,
      Medicine, Nursing and Midwifery, Pharmacy, Planning, Psychological Science,
      Science, Social Work, Sustainability and Veterinary Science. We aim to give
      graduates the qualifications and skills they need for the global workforce.</p>
    </div>
    <div class="tab-pane fade" id="profile" role="tabpanel" aria-labelledBy="profile-tab">
      <h2>Profile panel</h2>
      <p>We also recognise our special obligation to be relevant to our own
      region and have forged close linkages into the economy and social fabric of the
      northern Queensland. We are dedicated to ensuring that our teaching, learning
      and research is not only of high quality, but also delivers practical benefits
      to the peoples and industries of the region.</p>
    </div>
    <div class="tab-pane fade" id="dropdown1" role="tabpanel" aria-labelledBy="dropdown1-tab">
      <h2>Staff panel</h2>
      <p>The University conducts nationally significant and internationally
      recognised research in areas such as marine sciences, biodiversity, tropical
      ecology and environments, global warming, tourism, and tropical medicine and
      public health care in under-served populations.</p>
    </div>
    <div class="tab-pane fade" id="dropdown2" role="tabpanel" aria-labelledBy="dropdown2-tab">
      <h2>Students panel</h2>
      <p>
    </div>
  </div>
</div>

