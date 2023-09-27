---
layout: post
title:  "DemoPage: Speech Enhancement with Complex-valued Wiener Filter"
date:   2023-09-26 18:10:25 +0900
categories: jekyll update
---

# Abstract

# Source code

# Audio demo
<div class="grid">
    <div class="header-row">
        <div class="col-1-4">
            <div class="table-header">Noisy speech</div>
        </div>
        <div class="col-1-4">
            <div class="table-header">Enhanced speech (without phase correction)</div>
        </div>
        <div class="col-1-4">
            <div class="table-header">Enhanced speech (with phase correction)</div>
        </div>
        <div class="col-1-4">
            <div class="table-header">Clean speech</div>
        </div>
    </div>
    <div class="content-row">
        <div class="col-1-4">
            <div class="table-content"><audio controls="control" src="/assets/audios/sample_11_y_bt.wav"></audio></div>
        </div>
        <div class="col-1-4">
            <div class="table-content"><audio controls="control" src="/assets/audios/sample_11_xHat1_bt.wav"></audio></div>
        </div>
        <div class="col-1-4">
            <div class="table-content"><audio controls="control" src="/assets/audios/sample_11_xHat2_bt.wav"></audio></div>
        </div>
        <div class="col-1-4">
            <div class="table-content"><audio controls="control" src="/assets/audios/sample_11_x_bt.wav"></audio></div>
        </div>
    </div>
    <div class="content-row">
        <div class="col-1-4">
            <div class="table-content"><audio controls="control" src="/assets/audios/sample_10_y_bt.wav"></audio></div>
        </div>
        <div class="col-1-4">
            <div class="table-content"><audio controls="control" src="/assets/audios/sample_10_xHat1_bt.wav"></audio></div>
        </div>
        <div class="col-1-4">
            <div class="table-content"><audio controls="control" src="/assets/audios/sample_10_xHat2_bt.wav"></audio></div>
        </div>
        <div class="col-1-4">
            <div class="table-content"><audio controls="control" src="/assets/audios/sample_10_x_bt.wav"></audio></div>
        </div>
    </div>
</div>
<style>
    [class*='col-'] {
        float: left;
    }
    .grid:after {
        content: "";
        display: table;
        clear: both;
    }
    .col-1-4 {
        width: 25%;
        flex: 1;
    }
    .table-header {
        font-weight: bold;
        text-align: center;
    }
    .table-content {
        text-align: center;
    }
    *, *:after, *:before {
        -webkit-box-sizing: border-box;
        -moz-box-sizing: border-box;
        box-sizing: border-box;
    }
</style>