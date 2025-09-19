---
layout: page
title: Demo page
permalink: /
---

<!-- ===== Page-only styles ===== -->
<style>
  .page-title { display: none; } /* Demo page 숨김 */

  .sidebar { display: none; }
  .content { max-width: 1280px; margin: 0 auto; padding: 2rem 1rem; }

  /* 공통 레이아웃 */
  .hero { text-align: center; margin: 1.25rem 0 2.5rem; }
  .hero h1 { font-size: 2.1rem; margin: 0 0 .25rem; line-height: 1.22; }
  .hero .sub { font-size: 1.07rem; color: #666; margin: 0.4rem 0 0.6rem; }
  .hero .authors { font-size: 1.07rem; color: #111; margin: 0; }

  .section-title { font-family: inherit; font-weight: 800; font-size: 1.6rem; margin: 3rem 0 1rem; }
  .section-sub { font-size: 1.00rem; color: #444; margin: .2rem 0 .5rem; line-height: 1.45; }

  .figure { text-align: center; margin: 1rem auto 2rem; }
  .figure img { max-width: 100%; height: auto; border: 1px solid #eee; border-radius: 8px; }

  .abstract { font-size: 1.07rem; line-height: 1.7; background: #fafafa; border: 1px solid #eee; border-radius: 10px; padding: 1rem 1.2rem; }

  /* 오디오 표 */
  table.audio-samples { border-collapse: collapse; margin: 1.5rem auto; text-align: center; width: 100%; }
  .audio-samples th, .audio-samples td { border: 1px solid #ccc; padding: 10px; }
  .audio-samples th { background: #f8f8f8; }
  audio { width: 200px; max-width: 100%; }
  @media (max-width: 900px) { audio { width: 160px; } }
  @media (max-width: 720px) { audio { width: 140px; } }

  .samples-desc {
  font-size: 1.2rem;   /* 설명만 크게 */
  color: #333;
  line-height: 1.55;
  }
</style>



<div class="hero">
  <h1>ADAPTIVE VECTOR QUANTIZATION FOR IMPROVED CONTENT PRESERVATION<br/>IN MULTILINGUAL VOICE CONVERSION</h1>
  <p class="sub">Submitted to ICASSP 2026</p>
  <p class="authors">Hyomin Kim, Seyun Um, Soojoong Hwang, Sungwoong Hwang, and Hong-Goo Kang</p>
</div>

<div>
  <div class="section-title">Proposed Method</div>
  <div class="figure">
    <img src="/assets/image/archi.png" alt="Proposed Method Architecture">
  </div>
</div>

<div>
  <div class="abstract">
   In voice conversion (VC), it is crucial to disentangle content and speaker style representations from input waveforms. Recent neural VC approaches typically leverage content-related information from latent features extracted by pre-trained self-supervised representation learning frameworks, followed by a k-means-based vector quantizer (VQ). While this strategy achieves competitive performance, it is suboptimal in terms of content preservation, particularly for languages with complex phoneme inventories. In this work, we investigate the effectiveness of incorporating a learnable VQ codebook for content-related features across different VC models in multilingual scenarios. Unlike static k-means clustering, the learnable codebook adaptively adjusts its clusters according to the input distribution, thereby producing more discriminative and stable content representations. Experimental evaluations on English and Korean datasets demonstrate the superiority of our proposed method.
  </div>
</div>

<div>
  <div class="section-title">Samples</div>
  <div class="samples-desc">
    We compare the k-means baseline with the proposed learnable codebook approach on two VC models for both English and Korean.<br/>
    Our learnable codebook yields higher intelligibility and more natural speech.
  </div>
</div>



## Baseline 1: StyleBook

<style>
  table.audio-samples {
    border-collapse: collapse;
    margin: 1.5rem auto;
    text-align: center;
  }
  .audio-samples th, .audio-samples td {
    border: 1px solid #ccc;
    padding: 10px;
    min-width: 150px;
    font-size: 1.15rem;
  }
  .audio-samples th {
    background: #f8f8f8;
  }
  audio {
    width: 140px;
  }
</style>

<table class="audio-samples">
  <thead>
    <tr>
      <th>Language</th>
      <th>Source</th>
      <th>Target</th>
      <th>k-means</th>
      <th>Learnable (Proposed)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">English</td>
      <td><audio controls src="/assets/audio/stylebook/eng_source/8463_294828_000038_000000.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/eng_target/1995_10.0sec_3.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kmeans/eng/8463_294828_000038_000000_1995_10.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/learn/eng/8463_294828_000038_000000_1995_10.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="/assets/audio/stylebook/eng_source/8463_294828_000049_000000.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/eng_target/1995_10.0sec_0.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kmeans/eng/8463_294828_000049_000000_1995_10.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/learn/eng/8463_294828_000049_000000_1995_10.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="/assets/audio/stylebook/eng_source/8463_294828_000054_000000.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/eng_target/1995_10.0sec_1.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kmeans/eng/8463_294828_000054_000000_1995_10.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/learn/eng/8463_294828_000054_000000_1995_10.wav"></audio></td>
    </tr>

    <tr>
      <td rowspan="3">Korean</td>
      <td><audio controls src="/assets/audio/stylebook/kor_source/F1_Novel1_2208.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kor_target/M6_10.0sec_19.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kmeans/kor/F1_Novel1_2208_M6_10.0sec_19_2cd85448.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/learn/kor/F1_Novel1_2208_M6_10.0sec_19_2cd85448.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="/assets/audio/stylebook/kor_source/F2_FairyTale1_298.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kor_target/F3_10.0sec_2.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kmeans/kor/F2_FairyTale1_298_F3_10.0sec_2_64d0f151.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/learn/kor/F2_FairyTale1_298_F3_10.0sec_2_64d0f151.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="/assets/audio/stylebook/kor_source/M6_FairyTale2_1873.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kor_target/F5_10.0sec_17.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/kmeans/kor/M6_FairyTale2_1873_F5_10.wav"></audio></td>
      <td><audio controls src="/assets/audio/stylebook/learn/kor/M6_FairyTale2_1873_F5_10.0sec_17_30861900.wav"></audio></td>
    </tr>
  </tbody>
</table>

## Baseline 2: SEF-VC

<table class="audio-samples">
  <thead>
    <tr>
      <th>Language</th>
      <th>Source</th>
      <th>Target</th>
      <th>k-means</th>
      <th>Learnable (Proposed)</th>
    </tr>
  </thead>
  <tbody>
    <!-- English Samples -->
    <tr>
      <td rowspan="3">English</td>
      <td><audio controls src="/assets/audio/sefvc/eng_source/237_126133_000019_000000.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/eng_target/3570_10.0sec_2.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kmeans/eng/237_126133_000019_000000_3570_10.0sec_2_d23f299c.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/learn/eng/237_126133_000019_000000_3570_10.0sec_2_d23f299c.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="/assets/audio/sefvc/eng_source/237_134493_000008_000006.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/eng_target/7127_10.0sec_18.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kmeans/eng/237_134493_000008_000006_7127_10.0sec_18_c45262ed.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/learn/eng/237_134493_000008_000006_7127_10.0sec_18_c45262ed.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="/assets/audio/sefvc/eng_source/1089_134686_000009_000000.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/eng_target/1320_10.0sec_6.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kmeans/eng/1089_134686_000009_000000_1320_10.0sec_6_b92e4870.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/learn/eng/1089_134686_000009_000000_1320_10.0sec_6_b92e4870.wav"></audio></td>
    </tr>

    <!-- Korean Samples -->
    <tr>
      <td rowspan="3">Korean</td>
      <td><audio controls src="/assets/audio/sefvc/kor_source/F3_FairyTale2_701.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kor_target/F4_10.0sec_7.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kmeans/kor/F3_FairyTale2_701_F4_10.0sec_7_1a138fde.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/learn/kor/F3_FairyTale2_701_F4_10.0sec_7_1a138fde.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="/assets/audio/sefvc/kor_source/F1_SelfHelp1_1420.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kor_target/M5_10.0sec_13.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kmeans/kor/F1_SelfHelp1_1420_M5_10.0sec_13_73bb8f38.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/learn/kor/F1_SelfHelp1_1420_M5_10.0sec_13_73bb8f38.wav"></audio></td>
    </tr>
    <tr>
      <td><audio controls src="/assets/audio/sefvc/kor_source/F1_Novel1_1602.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kor_target/M4_10.0sec_15.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/kmeans/kor/F1_Novel1_1602_M4_10.0sec_15_52ad4337.wav"></audio></td>
      <td><audio controls src="/assets/audio/sefvc/learn/kor/F1_Novel1_1602_M4_10.0sec_15_52ad4337.wav"></audio></td>
    </tr>
  </tbody>
</table>

