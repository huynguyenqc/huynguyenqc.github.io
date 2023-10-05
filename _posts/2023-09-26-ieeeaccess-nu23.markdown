---
layout: post
title:  "Speech Enhancement with Complex-valued Wiener Filter"
date:   2023-09-26 18:10:25 +0900
categories: jekyll update
---

<!-- ## Abstract -->

## Source code
[SE-ComplexWiener](https://github.com/huynguyenqc/SE-ComplexWiener)

## Audio demo
{% assign fileNameList = "p232_005,p232_126,p232_182,p232_261,p232_373,p257_033,p257_179,p257_251,p257_347,p257_403" | split:"," %}

<div class="container-fluid">
  <div class="row">
    <div class="col-1 center-block" style="border-bottom: solid 1px black;"><div class="table-header">Sample</div></div>
    <div class="col-2 center-block noisy-column" style="border-bottom: solid 1px black;"><div class="table-header">Noisy</div></div>
    <div class="col-2 center-block enhanced-column-1" style="border-bottom: solid 1px black;"><div class="table-header">Enhanced (w/o \(e^{j\hat{\varphi}}\), w/o \(\mathcal{L}_{\mathrm{F0}}\))</div></div>
    <div class="col-2 center-block enhanced-column-2" style="border-bottom: solid 1px black;"><div class="table-header">Enhanced (with \(e^{j\hat{\varphi}}\), w/o \(\mathcal{L}_{\mathrm{F0}}\))</div></div>
    <div class="col-2 center-block enhanced-column-3" style="border-bottom: solid 1px black;"><div class="table-header">Enhanced (with \(e^{j\hat{\varphi}}\), with \(\mathcal{L}_{\mathrm{F0}}\))</div></div>
    <div class="col-2 center-block clean-column" style="border-bottom: solid 1px black;"><div class="table-header">Clean</div></div>
  </div>
  {% for fileName in fileNameList %}
  <div class="row">
    <div class="col-1 center-block" align="center"><div class="vertical-center" style="text-align: center;">{{ fileName }}</div></div>
    <div class="col-2 center-block noisy-column" align="center"><audio class="audio-demo" controls="control" src="/assets/audios/demo_samples/noisy/{{ fileName }}.wav" ></audio></div>
    <div class="col-2 center-block enhanced-column-1" align="center"><audio class="audio-demo" controls="control" src="/assets/audios/demo_samples/dIS/{{ fileName }}.wav"></audio></div>
    <div class="col-2 center-block enhanced-column-2" align="center"><audio class="audio-demo" controls="control" src="/assets/audios/demo_samples/dIS_phase/{{ fileName }}.wav"></audio></div>
    <div class="col-2 center-block enhanced-column-3" align="center"><audio class="audio-demo" controls="control" src="/assets/audios/demo_samples/dIS_phase_F0/{{ fileName }}.wav"></audio></div>
    <div class="col-2 center-block clean-column" align="center"><audio class="audio-demo" controls="control" src="/assets/audios/demo_samples/clean/{{ fileName }}.wav"></audio></div>
  </div>
  {% endfor %}
</div>
<style>
    .table-header {
        text-align: center;
        font-weight: bold;
    }
    .audio-demo {
        width: 100%;
    }
    .noisy-column {
        background-color: #d7ded9;
    }
    .enhanced-column-1 {
        background-color: #c6f7d4;
    }
    .enhanced-column-2 {
        background-color: #d6f7e4;
    }
    .enhanced-column-3 {
        background-color: #e6f7f4;
    }
    .clean-column {
        background-color: #c2c6ed;
    }
    div.col-2{
        padding-top: 10px;
        padding-bottom: 10px;
    }
    div.col-1{
        padding-top: 10px;
        padding-bottom: 10px;
    }
    .vertical-center {
        margin: 0;
        position: absolute;
        top: 50%;
        -ms-transform: translateY(-50%);
        transform: translateY(-50%);
    }
    .jekyll-linkpreview-wrapper {
        max-width: 600px;
        margin-bottom: 20px;
    }
    .jekyll-linkpreview-wrapper-inner {
        border: 1px solid rgba(0,0,0,.1);
        padding: 12px;
    }
    .jekyll-linkpreview-content {
        position: relative;
        height: 100px;
        overflow: hidden;
        margin-bottom: 10px;
    }
    .jekyll-linkpreview-image {
        position: absolute;
        top: 0;
        right: 0;
    }
    .jekyll-linkpreview-image img {
        width: 100px;
        height: 100px;
    }
    .jekyll-linkpreview-body {
        margin-right: 110px;
    }
    .jekyll-linkpreview-body-nog {
        margin-right: 10px;
    }
    .jekyll-linkpreview-title {
        font-size: 17px;
        margin: 0 0 2px;
        line-height: 1.3;
    }
    .jekyll-linkpreview-description {
        line-height: 1.5;
        font-size: 13px;
    }
    .jekyll-linkpreview-footer {
        font-size: 11px;
    }
</style>