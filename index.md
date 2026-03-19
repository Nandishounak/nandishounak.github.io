---
layout: default
title: Shounak Nandi
---

<div class="hero">
  <div class="photo-col">
    <img id="profile-photo" class="profile-photo" src="" alt="Shounak Nandi"
    style="display:none;">
    <button id="refresh-photo" class="refresh-btn" title="Show another photo">&#x21bb;</button>
  </div>

  <div>
    <h1>Shounak Nandi</h1>

    <p class="muted">
      Neuroimaging Researcher<br>
      New York City, USA
    </p>

    <p>
      I am a neuroimaging researcher working on multi-modal MRI analysis, diffusion microstructure modeling,
      low-field and accessible MRI, and scalable neuroimaging pipelines on HPC systems.
    </p>

    <p>
      My work spans diffusion MRI, fMRI, ASL, and structural MRI, with an emphasis on reproducibility,
      computational efficiency, and clinically meaningful imaging biomarkers.
    </p>

    <p style="display:flex; gap:14px; flex-wrap:wrap;">
      <a href="{{ '/assets/CV.pdf' | relative_url }}">CV</a>
      <a href="https://github.com/nandishounak">GitHub</a>
      <a href="https://www.linkedin.com/in/shounak-nandi-b2b40b78/">LinkedIn</a>
      <a href="https://scholar.google.com/citations?user=nqoO0iwAAAAJ&hl=en">Google Scholar</a>
      <a href="https://orcid.org/0000-0003-3588-3838">ORCID</a>
      <a href="mailto:nandishounak2011@gmail.com">Email</a>
    </p>
  </div>
</div>

## About

I am currently a **Study Coordinator** in Radiology at Albert Einstein College of Medicine in New York. My research focuses on diffusion MRI, low-field MRI, multimodal imaging workflows, and reproducible computational pipelines. Previously, I worked with the Accessible MR Laboratory at Johns Hopkins University School of Medicine and Icahn School of Medicine at Mount Sinai. I hold an M.Sc. in Biomedical Engineering & Medical Physics from the Technical University of Munich.

## Research Interests

- &bull;  
  Diffusion MRI microstructure modeling
- &bull;  
  Low-field and accessible MRI
- &bull;  
  Multimodal neuroimaging preprocessing
- &bull;  
  Quantitative imaging biomarkers
- &bull;  
  Reproducible pipelines and HPC workflows
- &bull;  
  Statistical analysis and machine learning for imaging

## Education

**M.Sc., Biomedical Engineering & Medical Physics** Technical University of Munich, Germany (2024)

**B.Tech., Biomedical Engineering** Maulana Abul Kalam Azad University of Technology, India (2017)

## Selected Updates

- &bull; **Feb 2026:** ISMRM abstracts accepted.
- &bull; **Jan 2026:** Paper 1 published.
- &bull; **Jan 2026:** Paper 2 published.

For more, see the [News]({{ '/news' | relative_url }}) and [Research]({{ '/research' | relative_url }}) pages.

## More About Me

Beyond research, I like to spend time in [music](https://www.youtube.com/@ShounakNandi), racquet sports, gym, and little bit to [photography](https://www.instagram.com/image_dot_jpeg/).

<script>
(function() {
  var photos = [
    "{{ '/assets/img/profile2.jpeg' | relative_url }}",
    "{{ '/assets/img/profile5.jpeg' | relative_url }}"
  ];
  function shuffle(arr) {
    for (var i = arr.length - 1; i > 0; i--) {
      var j = Math.floor(Math.random() * (i + 1));
      var tmp = arr[i]; arr[i] = arr[j]; arr[j] = tmp;
    }
    return arr;
  }
  var currentSrc = null;
  function loadPhoto(list, startIndex, imgEl, onDone) {
    if (startIndex >= list.length) { if (onDone) onDone(false); return; }
    var tester = new Image();
    tester.onload = function() {
      imgEl.src = this.src;
      imgEl.style.display = 'block';
      currentSrc = list[startIndex];
      if (onDone) onDone(true);
    };
    tester.onerror = function() { loadPhoto(list, startIndex + 1, imgEl, onDone); };
    tester.src = list[startIndex];
  }
  var img = document.getElementById('profile-photo');
  var btn = document.getElementById('refresh-photo');
  if (!img) return;
  loadPhoto(shuffle(photos.slice()), 0, img, null);
  if (btn) {
    var busy = false;
    btn.addEventListener('click', function() {
      if (busy) return;
      busy = true;
      btn.style.transition = 'transform 0.4s ease';
      btn.style.transform = 'rotate(360deg)';
      setTimeout(function() { btn.style.transform = ''; btn.style.transition = ''; }, 400);
      var others = photos.filter(function(p) { return p !== currentSrc; });
      if (others.length === 0) others = photos.slice();
      loadPhoto(shuffle(others), 0, img, function() { busy = false; });
    });
  }
})();
</script>
