---
layout: default
title: Shounak Nandi
---

<div class="hero">
  <img id="profile-photo" class="profile-photo" src="{{ '/assets/img/profile2.jpeg' | relative_url }}" alt="Shounak Nandi">

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

    <div class="links">
      <a href="{{ '/assets/CV.pdf' | relative_url }}">CV</a>
      <a href="https://github.com/nandishounak">GitHub</a>
      <a href="https://www.linkedin.com/in/shounak-nandi-b2b40b78/">LinkedIn</a>
      <a href="https://scholar.google.com/citations?user=nqoO0iwAAAAJ&hl=en">Google Scholar</a>
      <a href="https://orcid.org/0000-0003-3588-3838">ORCID</a>
      <a href="mailto:nandishounak2011@gmail.com">Email</a>
    </div>
  </div>
</div>

## About

I am currently a **Study Coordinator** in Radiology at Albert Einstein College of Medicine in New York.
My research focuses on diffusion MRI, low-field MRI, multimodal imaging workflows, and reproducible computational pipelines.
Previously, I worked with the Accessible MR Laboratory at Johns Hopkins University School of Medicine and Icahn School of Medicine at Mount Sinai.
I hold an M.Sc. in Biomedical Engineering & Medical Physics from the Technical University of Munich.

## Research Interests

- Diffusion MRI microstructure modeling
- Low-field and accessible MRI
- Multimodal neuroimaging preprocessing
- Quantitative imaging biomarkers
- Reproducible pipelines and HPC workflows
- Statistical analysis and machine learning for imaging

## Education

**M.Sc., Biomedical Engineering & Medical Physics**
Technical University of Munich, Germany (2024)

**B.Tech., Biomedical Engineering**
Maulana Abul Kalam Azad University of Technology, India (2017)

## Selected Updates

- **Feb 2026:** ISMRM abstracts accepted.
- **Jan 2026:** Paper 1 published.
- **Jan 2026:** Paper 2 published.

For more, see the [News]({{ '/news' | relative_url }}) and [Research]({{ '/research' | relative_url }}) pages.

<script>
var photos = [
  "{{ '/assets/img/profile2.jpeg' | relative_url }}",
  "{{ '/assets/img/profile3.jpeg' | relative_url }}",
  "{{ '/assets/img/profile7.jpeg' | relative_url }}"
];
var img = document.getElementById('profile-photo');
if (img) {
  img.src = photos[Math.floor(Math.random() * photos.length)];
}
</script>
