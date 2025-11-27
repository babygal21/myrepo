<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"><head>

<meta charset="utf-8">
<meta name="generator" content="quarto-1.6.42">

<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">


<title>Replication Project</title>
<style>
code{white-space: pre-wrap;}
span.smallcaps{font-variant: small-caps;}
div.columns{display: flex; gap: min(4vw, 1.5em);}
div.column{flex: auto; overflow-x: auto;}
div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
ul.task-list{list-style: none;}
ul.task-list li input[type="checkbox"] {
  width: 0.8em;
  margin: 0 0.8em 0.2em -1em; /* quarto-specific, see https://github.com/quarto-dev/quarto-cli/issues/4556 */ 
  vertical-align: middle;
}
/* CSS for syntax highlighting */
pre > code.sourceCode { white-space: pre; position: relative; }
pre > code.sourceCode > span { line-height: 1.25; }
pre > code.sourceCode > span:empty { height: 1.2em; }
.sourceCode { overflow: visible; }
code.sourceCode > span { color: inherit; text-decoration: inherit; }
div.sourceCode { margin: 1em 0; }
pre.sourceCode { margin: 0; }
@media screen {
div.sourceCode { overflow: auto; }
}
@media print {
pre > code.sourceCode { white-space: pre-wrap; }
pre > code.sourceCode > span { display: inline-block; text-indent: -5em; padding-left: 5em; }
}
pre.numberSource code
  { counter-reset: source-line 0; }
pre.numberSource code > span
  { position: relative; left: -4em; counter-increment: source-line; }
pre.numberSource code > span > a:first-child::before
  { content: counter(source-line);
    position: relative; left: -1em; text-align: right; vertical-align: baseline;
    border: none; display: inline-block;
    -webkit-touch-callout: none; -webkit-user-select: none;
    -khtml-user-select: none; -moz-user-select: none;
    -ms-user-select: none; user-select: none;
    padding: 0 4px; width: 4em;
  }
pre.numberSource { margin-left: 3em;  padding-left: 4px; }
div.sourceCode
  {   }
@media screen {
pre > code.sourceCode > span > a:first-child::before { text-decoration: underline; }
}
</style>


<script src="replicationproject_files/libs/clipboard/clipboard.min.js"></script>
<script src="replicationproject_files/libs/quarto-html/quarto.js"></script>
<script src="replicationproject_files/libs/quarto-html/popper.min.js"></script>
<script src="replicationproject_files/libs/quarto-html/tippy.umd.min.js"></script>
<script src="replicationproject_files/libs/quarto-html/anchor.min.js"></script>
<link href="replicationproject_files/libs/quarto-html/tippy.css" rel="stylesheet">
<link href="replicationproject_files/libs/quarto-html/quarto-syntax-highlighting-2f5df379a58b258e96c21c0638c20c03.css" rel="stylesheet" id="quarto-text-highlighting-styles">
<script src="replicationproject_files/libs/bootstrap/bootstrap.min.js"></script>
<link href="replicationproject_files/libs/bootstrap/bootstrap-icons.css" rel="stylesheet">
<link href="replicationproject_files/libs/bootstrap/bootstrap-1bc8a17f135ab3d594c857e9f48e611b.min.css" rel="stylesheet" append-hash="true" id="quarto-bootstrap" data-mode="light">


</head>

<body class="fullcontent">

<div id="quarto-content" class="page-columns page-rows-contents page-layout-article">

<main class="content" id="quarto-document-content">

<header id="title-block-header" class="quarto-title-block default">
<div class="quarto-title">
<h1 class="title">Replication Project</h1>
</div>



<div class="quarto-title-meta">

    
  
    
  </div>
  


</header>


<section id="my-replication" class="level2">
<h2 class="anchored" data-anchor-id="my-replication">My Replication</h2>
<div class="cell" data-layout-align="center">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(tidyverse)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>── Attaching core tidyverse packages ──────────────────────── tidyverse 2.0.0 ──
✔ dplyr     1.1.4     ✔ readr     2.1.5
✔ forcats   1.0.0     ✔ stringr   1.5.1
✔ ggplot2   4.0.0     ✔ tibble    3.3.0
✔ lubridate 1.9.4     ✔ tidyr     1.3.1
✔ purrr     1.1.0     
── Conflicts ────────────────────────────────────────── tidyverse_conflicts() ──
✖ dplyr::filter() masks stats::filter()
✖ dplyr::lag()    masks stats::lag()
ℹ Use the conflicted package (&lt;http://conflicted.r-lib.org/&gt;) to force all conflicts to become errors</code></pre>
</div>
<div class="sourceCode cell-code" id="cb3"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a><span class="fu">library</span>(scales)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>
Attaching package: 'scales'

The following object is masked from 'package:purrr':

    discard

The following object is masked from 'package:readr':

    col_factor</code></pre>
</div>
<div class="sourceCode cell-code" id="cb5"><pre class="sourceCode r code-with-copy"><code class="sourceCode r"><span id="cb5-1"><a href="#cb5-1" aria-hidden="true" tabindex="-1"></a>df_recon1 <span class="ot">&lt;-</span> <span class="fu">tribble</span>(</span>
<span id="cb5-2"><a href="#cb5-2" aria-hidden="true" tabindex="-1"></a>  <span class="sc">~</span>year, <span class="sc">~</span>country, <span class="sc">~</span>sector, <span class="sc">~</span>count,</span>
<span id="cb5-3"><a href="#cb5-3" aria-hidden="true" tabindex="-1"></a>  <span class="co"># 2018</span></span>
<span id="cb5-4"><a href="#cb5-4" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2018</span>, <span class="st">"Greece"</span>, <span class="st">"Government"</span>, <span class="dv">1</span>,</span>
<span id="cb5-5"><a href="#cb5-5" aria-hidden="true" tabindex="-1"></a>  <span class="co"># 2019</span></span>
<span id="cb5-6"><a href="#cb5-6" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2019</span>, <span class="st">"Bulgaria"</span>, <span class="st">"Government"</span>, <span class="dv">1</span>,</span>
<span id="cb5-7"><a href="#cb5-7" aria-hidden="true" tabindex="-1"></a>  <span class="co">#2020</span></span>
<span id="cb5-8"><a href="#cb5-8" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2020</span>, <span class="st">"Finland"</span>, <span class="st">"Energy"</span>, <span class="dv">1</span>,</span>
<span id="cb5-9"><a href="#cb5-9" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2020</span>, <span class="st">"Finland"</span>, <span class="st">"Transport"</span>, <span class="dv">1</span>,</span>
<span id="cb5-10"><a href="#cb5-10" aria-hidden="true" tabindex="-1"></a>  <span class="co"># 2022</span></span>
<span id="cb5-11"><a href="#cb5-11" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Albania"</span>, <span class="st">"Military"</span>, <span class="dv">1</span>,</span>
<span id="cb5-12"><a href="#cb5-12" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Bosnia - Herzegovina"</span>, <span class="st">"Government"</span>, <span class="dv">2</span>,</span>
<span id="cb5-13"><a href="#cb5-13" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Bulgaria"</span>, <span class="st">"Military"</span>, <span class="dv">2</span>,</span>
<span id="cb5-14"><a href="#cb5-14" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Bulgaria"</span>, <span class="st">"Transport"</span>, <span class="dv">1</span>,</span>
<span id="cb5-15"><a href="#cb5-15" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Denmark"</span>, <span class="st">"Energy"</span>, <span class="dv">1</span>,</span>
<span id="cb5-16"><a href="#cb5-16" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Finland"</span>, <span class="st">"Government"</span>, <span class="dv">1</span>,</span>
<span id="cb5-17"><a href="#cb5-17" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Germany"</span>, <span class="st">"Military"</span>, <span class="dv">1</span>,</span>
<span id="cb5-18"><a href="#cb5-18" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Italy"</span>, <span class="st">"Communications"</span>, <span class="dv">1</span>,</span>
<span id="cb5-19"><a href="#cb5-19" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Norway"</span>, <span class="st">"Energy"</span>, <span class="dv">3</span>,</span>
<span id="cb5-20"><a href="#cb5-20" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2022</span>, <span class="st">"Poland"</span>, <span class="st">"Government"</span>, <span class="dv">1</span>,</span>
<span id="cb5-21"><a href="#cb5-21" aria-hidden="true" tabindex="-1"></a>  <span class="co"># 2023</span></span>
<span id="cb5-22"><a href="#cb5-22" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2023</span>, <span class="st">"Bulgaria"</span>, <span class="st">"Military"</span>, <span class="dv">2</span>,</span>
<span id="cb5-23"><a href="#cb5-23" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2023</span>, <span class="st">"Estonia"</span>, <span class="st">"Undersea"</span>, <span class="dv">1</span>,</span>
<span id="cb5-24"><a href="#cb5-24" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2023</span>, <span class="st">"Czech Republic"</span>, <span class="st">"Government"</span>, <span class="dv">1</span>,</span>
<span id="cb5-25"><a href="#cb5-25" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2023</span>, <span class="st">"Germany"</span>, <span class="st">"Energy"</span>, <span class="dv">1</span>,</span>
<span id="cb5-26"><a href="#cb5-26" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2023</span>, <span class="st">"Poland"</span>, <span class="st">"Transport"</span>, <span class="dv">4</span>,</span>
<span id="cb5-27"><a href="#cb5-27" aria-hidden="true" tabindex="-1"></a>  <span class="co"># 2024</span></span>
<span id="cb5-28"><a href="#cb5-28" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Czech Republic"</span>, <span class="st">"Transport"</span>, <span class="dv">1</span>,</span>
<span id="cb5-29"><a href="#cb5-29" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Denmark"</span>, <span class="st">"Water"</span>, <span class="dv">1</span>,</span>
<span id="cb5-30"><a href="#cb5-30" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Finland"</span>, <span class="st">"Undersea"</span>, <span class="dv">1</span>,</span>
<span id="cb5-31"><a href="#cb5-31" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Finland"</span>, <span class="st">"Water"</span>, <span class="dv">6</span>,</span>
<span id="cb5-32"><a href="#cb5-32" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"France"</span>, <span class="st">"Transport"</span>, <span class="dv">3</span>,</span>
<span id="cb5-33"><a href="#cb5-33" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"France"</span>, <span class="st">"Water"</span>, <span class="dv">1</span>,</span>
<span id="cb5-34"><a href="#cb5-34" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Germany"</span>, <span class="st">"Military"</span>, <span class="dv">5</span>,</span>
<span id="cb5-35"><a href="#cb5-35" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Germany"</span>, <span class="st">"Water"</span>, <span class="dv">2</span>,</span>
<span id="cb5-36"><a href="#cb5-36" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Norway"</span>, <span class="st">"Communications"</span>, <span class="dv">1</span>,</span>
<span id="cb5-37"><a href="#cb5-37" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Norway"</span>, <span class="st">"Military"</span>, <span class="dv">1</span>,</span>
<span id="cb5-38"><a href="#cb5-38" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Poland"</span>, <span class="st">"Military"</span>, <span class="dv">1</span>,</span>
<span id="cb5-39"><a href="#cb5-39" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Poland"</span>, <span class="st">"Undersea"</span>, <span class="dv">1</span>,</span>
<span id="cb5-40"><a href="#cb5-40" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Poland"</span>, <span class="st">"Water"</span>, <span class="dv">1</span>,</span>
<span id="cb5-41"><a href="#cb5-41" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Romania"</span>, <span class="st">"Health"</span>, <span class="dv">1</span>,</span>
<span id="cb5-42"><a href="#cb5-42" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Slovakia"</span>, <span class="st">"Military"</span>, <span class="dv">1</span>,</span>
<span id="cb5-43"><a href="#cb5-43" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Spain"</span>, <span class="st">"Industry"</span>, <span class="dv">1</span>,</span>
<span id="cb5-44"><a href="#cb5-44" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Sweden"</span>, <span class="st">"Communications"</span>, <span class="dv">1</span>,</span>
<span id="cb5-45"><a href="#cb5-45" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Sweden"</span>, <span class="st">"Undersea"</span>, <span class="dv">1</span>,</span>
<span id="cb5-46"><a href="#cb5-46" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"Sweden"</span>, <span class="st">"Water"</span>, <span class="dv">1</span>,</span>
<span id="cb5-47"><a href="#cb5-47" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"UK"</span>, <span class="st">"Health"</span>, <span class="dv">1</span>,</span>
<span id="cb5-48"><a href="#cb5-48" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2024</span>, <span class="st">"UK"</span>, <span class="st">"Industry"</span>, <span class="dv">1</span>,</span>
<span id="cb5-49"><a href="#cb5-49" aria-hidden="true" tabindex="-1"></a>  <span class="co"># 2025</span></span>
<span id="cb5-50"><a href="#cb5-50" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Baltic Sea"</span>, <span class="st">"Undersea"</span>, <span class="dv">1</span>,</span>
<span id="cb5-51"><a href="#cb5-51" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Czech Republic"</span>, <span class="st">"Military"</span>, <span class="dv">1</span>,</span>
<span id="cb5-52"><a href="#cb5-52" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Germany"</span>, <span class="st">"Military"</span>, <span class="dv">1</span>,</span>
<span id="cb5-53"><a href="#cb5-53" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Germany"</span>, <span class="st">"Transport"</span>, <span class="dv">1</span>,</span>
<span id="cb5-54"><a href="#cb5-54" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Germany"</span>, <span class="st">"Undersea"</span>, <span class="dv">1</span>,</span>
<span id="cb5-55"><a href="#cb5-55" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Greece"</span>, <span class="st">"Energy"</span>, <span class="dv">1</span>,</span>
<span id="cb5-56"><a href="#cb5-56" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Netherlands"</span>, <span class="st">"Transport"</span>, <span class="dv">1</span>,</span>
<span id="cb5-57"><a href="#cb5-57" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Norway"</span>, <span class="st">"Energy"</span>, <span class="dv">1</span>,</span>
<span id="cb5-58"><a href="#cb5-58" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Serbia"</span>, <span class="st">"Military"</span>, <span class="dv">1</span>,</span>
<span id="cb5-59"><a href="#cb5-59" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Sweden"</span>, <span class="st">"Undersea"</span>, <span class="dv">1</span>,</span>
<span id="cb5-60"><a href="#cb5-60" aria-hidden="true" tabindex="-1"></a>  <span class="dv">2025</span>, <span class="st">"Sweden"</span>, <span class="st">"Water"</span>, <span class="dv">1</span></span>
<span id="cb5-61"><a href="#cb5-61" aria-hidden="true" tabindex="-1"></a>)</span>
<span id="cb5-62"><a href="#cb5-62" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-63"><a href="#cb5-63" aria-hidden="true" tabindex="-1"></a>df <span class="ot">&lt;-</span> df_recon1 <span class="sc">|&gt;</span></span>
<span id="cb5-64"><a href="#cb5-64" aria-hidden="true" tabindex="-1"></a>  <span class="fu">arrange</span>(year, country, <span class="fu">row_number</span>()) <span class="sc">|&gt;</span></span>
<span id="cb5-65"><a href="#cb5-65" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(year, country) <span class="sc">|&gt;</span></span>
<span id="cb5-66"><a href="#cb5-66" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(</span>
<span id="cb5-67"><a href="#cb5-67" aria-hidden="true" tabindex="-1"></a>    <span class="at">ymin =</span> <span class="fu">c</span>(<span class="dv">0</span>, <span class="fu">cumsum</span>(count)[<span class="sc">-</span><span class="fu">n</span>()]),</span>
<span id="cb5-68"><a href="#cb5-68" aria-hidden="true" tabindex="-1"></a>    <span class="at">ymax =</span> <span class="fu">cumsum</span>(count)</span>
<span id="cb5-69"><a href="#cb5-69" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">|&gt;</span></span>
<span id="cb5-70"><a href="#cb5-70" aria-hidden="true" tabindex="-1"></a>  <span class="fu">ungroup</span>() <span class="sc">|&gt;</span></span>
<span id="cb5-71"><a href="#cb5-71" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">xlabel =</span> <span class="fu">paste0</span>(country, <span class="st">"</span><span class="sc">\n</span><span class="st">"</span>, year))</span>
<span id="cb5-72"><a href="#cb5-72" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-73"><a href="#cb5-73" aria-hidden="true" tabindex="-1"></a>desired_order <span class="ot">&lt;-</span> df <span class="sc">|&gt;</span></span>
<span id="cb5-74"><a href="#cb5-74" aria-hidden="true" tabindex="-1"></a>  <span class="fu">distinct</span>(xlabel, year, country) <span class="sc">|&gt;</span></span>
<span id="cb5-75"><a href="#cb5-75" aria-hidden="true" tabindex="-1"></a>  <span class="fu">arrange</span>(year, country) <span class="sc">|&gt;</span></span>
<span id="cb5-76"><a href="#cb5-76" aria-hidden="true" tabindex="-1"></a>  <span class="fu">pull</span>(xlabel)</span>
<span id="cb5-77"><a href="#cb5-77" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-78"><a href="#cb5-78" aria-hidden="true" tabindex="-1"></a>df<span class="sc">$</span>xlabel <span class="ot">&lt;-</span> <span class="fu">factor</span>(df<span class="sc">$</span>xlabel, <span class="at">levels =</span> desired_order)</span>
<span id="cb5-79"><a href="#cb5-79" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-80"><a href="#cb5-80" aria-hidden="true" tabindex="-1"></a>sector_colors <span class="ot">&lt;-</span> <span class="fu">c</span>(</span>
<span id="cb5-81"><a href="#cb5-81" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Communications"</span> <span class="ot">=</span> <span class="st">"#9CCCA6"</span>,</span>
<span id="cb5-82"><a href="#cb5-82" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Energy"</span> <span class="ot">=</span> <span class="st">"#EAA65A"</span>,</span>
<span id="cb5-83"><a href="#cb5-83" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Government"</span> <span class="ot">=</span> <span class="st">"#264A7A"</span>,</span>
<span id="cb5-84"><a href="#cb5-84" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Health"</span> <span class="ot">=</span> <span class="st">"#DCECCB"</span>,</span>
<span id="cb5-85"><a href="#cb5-85" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Industry"</span> <span class="ot">=</span> <span class="st">"#BFC0C1"</span>,</span>
<span id="cb5-86"><a href="#cb5-86" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Military"</span> <span class="ot">=</span> <span class="st">"#5B6B4F"</span>,</span>
<span id="cb5-87"><a href="#cb5-87" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Transport"</span> <span class="ot">=</span> <span class="st">"#D98E80"</span>,</span>
<span id="cb5-88"><a href="#cb5-88" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Undersea"</span> <span class="ot">=</span> <span class="st">"#6E83B3"</span>,</span>
<span id="cb5-89"><a href="#cb5-89" aria-hidden="true" tabindex="-1"></a>  <span class="st">"Water"</span> <span class="ot">=</span> <span class="st">"#90C6F6"</span></span>
<span id="cb5-90"><a href="#cb5-90" aria-hidden="true" tabindex="-1"></a>)</span>
<span id="cb5-91"><a href="#cb5-91" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-92"><a href="#cb5-92" aria-hidden="true" tabindex="-1"></a>df<span class="sc">$</span>sector <span class="ot">&lt;-</span> <span class="fu">factor</span>(</span>
<span id="cb5-93"><a href="#cb5-93" aria-hidden="true" tabindex="-1"></a>  df<span class="sc">$</span>sector,</span>
<span id="cb5-94"><a href="#cb5-94" aria-hidden="true" tabindex="-1"></a>  <span class="at">levels =</span> <span class="fu">c</span>(</span>
<span id="cb5-95"><a href="#cb5-95" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Communications"</span>,</span>
<span id="cb5-96"><a href="#cb5-96" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Energy"</span>,</span>
<span id="cb5-97"><a href="#cb5-97" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Government"</span>,</span>
<span id="cb5-98"><a href="#cb5-98" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Health"</span>,</span>
<span id="cb5-99"><a href="#cb5-99" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Industry"</span>,</span>
<span id="cb5-100"><a href="#cb5-100" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Military"</span>,</span>
<span id="cb5-101"><a href="#cb5-101" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Transport"</span>,</span>
<span id="cb5-102"><a href="#cb5-102" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Undersea"</span>,</span>
<span id="cb5-103"><a href="#cb5-103" aria-hidden="true" tabindex="-1"></a>    <span class="st">"Water"</span>))</span>
<span id="cb5-104"><a href="#cb5-104" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-105"><a href="#cb5-105" aria-hidden="true" tabindex="-1"></a>df<span class="sc">$</span>sector <span class="ot">&lt;-</span> <span class="fu">factor</span>(df<span class="sc">$</span>sector, <span class="at">levels =</span> <span class="fu">names</span>(sector_colors))</span>
<span id="cb5-106"><a href="#cb5-106" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-107"><a href="#cb5-107" aria-hidden="true" tabindex="-1"></a>year_positions <span class="ot">&lt;-</span> df <span class="sc">|&gt;</span></span>
<span id="cb5-108"><a href="#cb5-108" aria-hidden="true" tabindex="-1"></a>  <span class="fu">distinct</span>(country, year, xlabel) <span class="sc">|&gt;</span></span>
<span id="cb5-109"><a href="#cb5-109" aria-hidden="true" tabindex="-1"></a>  <span class="fu">arrange</span>(year, xlabel) <span class="sc">|&gt;</span></span>
<span id="cb5-110"><a href="#cb5-110" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(year) <span class="sc">|&gt;</span></span>
<span id="cb5-111"><a href="#cb5-111" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarize</span>(</span>
<span id="cb5-112"><a href="#cb5-112" aria-hidden="true" tabindex="-1"></a>    <span class="at">x =</span> <span class="fu">mean</span>(<span class="fu">as.numeric</span>(<span class="fu">factor</span>(xlabel, <span class="at">levels =</span> <span class="fu">levels</span>(df<span class="sc">$</span>xlabel))))</span>
<span id="cb5-113"><a href="#cb5-113" aria-hidden="true" tabindex="-1"></a>  )</span>
<span id="cb5-114"><a href="#cb5-114" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-115"><a href="#cb5-115" aria-hidden="true" tabindex="-1"></a>year_boundaries <span class="ot">&lt;-</span> df <span class="sc">|&gt;</span></span>
<span id="cb5-116"><a href="#cb5-116" aria-hidden="true" tabindex="-1"></a>  <span class="fu">distinct</span>(year, xlabel) <span class="sc">|&gt;</span></span>
<span id="cb5-117"><a href="#cb5-117" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(<span class="at">x =</span> <span class="fu">as.numeric</span>(<span class="fu">factor</span>(xlabel, <span class="at">levels =</span> <span class="fu">levels</span>(df<span class="sc">$</span>xlabel)))) <span class="sc">|&gt;</span></span>
<span id="cb5-118"><a href="#cb5-118" aria-hidden="true" tabindex="-1"></a>  <span class="fu">group_by</span>(year) <span class="sc">|&gt;</span></span>
<span id="cb5-119"><a href="#cb5-119" aria-hidden="true" tabindex="-1"></a>  <span class="fu">summarize</span>(</span>
<span id="cb5-120"><a href="#cb5-120" aria-hidden="true" tabindex="-1"></a>    <span class="at">min_x =</span> <span class="fu">min</span>(x),</span>
<span id="cb5-121"><a href="#cb5-121" aria-hidden="true" tabindex="-1"></a>    <span class="at">max_x =</span> <span class="fu">max</span>(x)</span>
<span id="cb5-122"><a href="#cb5-122" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">|&gt;</span></span>
<span id="cb5-123"><a href="#cb5-123" aria-hidden="true" tabindex="-1"></a>  <span class="fu">arrange</span>(year) <span class="sc">|&gt;</span></span>
<span id="cb5-124"><a href="#cb5-124" aria-hidden="true" tabindex="-1"></a>  <span class="fu">mutate</span>(</span>
<span id="cb5-125"><a href="#cb5-125" aria-hidden="true" tabindex="-1"></a>    <span class="at">boundary_x =</span> <span class="fu">lag</span>(max_x) <span class="sc">+</span> <span class="fl">0.5</span></span>
<span id="cb5-126"><a href="#cb5-126" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">|&gt;</span></span>
<span id="cb5-127"><a href="#cb5-127" aria-hidden="true" tabindex="-1"></a>  <span class="fu">filter</span>(<span class="sc">!</span><span class="fu">is.na</span>(boundary_x))</span>
<span id="cb5-128"><a href="#cb5-128" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb5-129"><a href="#cb5-129" aria-hidden="true" tabindex="-1"></a><span class="fu">ggplot</span>(df) <span class="sc">+</span></span>
<span id="cb5-130"><a href="#cb5-130" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_text</span>(</span>
<span id="cb5-131"><a href="#cb5-131" aria-hidden="true" tabindex="-1"></a>    <span class="at">data =</span> year_positions,</span>
<span id="cb5-132"><a href="#cb5-132" aria-hidden="true" tabindex="-1"></a>    <span class="fu">aes</span>(<span class="at">x =</span> x, <span class="at">y =</span> <span class="dv">0</span>, <span class="at">label =</span> year),</span>
<span id="cb5-133"><a href="#cb5-133" aria-hidden="true" tabindex="-1"></a>    <span class="at">vjust =</span> <span class="dv">1</span>,</span>
<span id="cb5-134"><a href="#cb5-134" aria-hidden="true" tabindex="-1"></a>    <span class="at">hjust =</span> <span class="dv">5</span>,</span>
<span id="cb5-135"><a href="#cb5-135" aria-hidden="true" tabindex="-1"></a>    <span class="at">angle =</span> <span class="dv">90</span>,</span>
<span id="cb5-136"><a href="#cb5-136" aria-hidden="true" tabindex="-1"></a>    <span class="at">size =</span> <span class="dv">3</span>,</span>
<span id="cb5-137"><a href="#cb5-137" aria-hidden="true" tabindex="-1"></a>    <span class="at">fontface =</span> <span class="st">"bold"</span></span>
<span id="cb5-138"><a href="#cb5-138" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">+</span></span>
<span id="cb5-139"><a href="#cb5-139" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_text</span>(</span>
<span id="cb5-140"><a href="#cb5-140" aria-hidden="true" tabindex="-1"></a>    <span class="at">data =</span> year_boundaries,</span>
<span id="cb5-141"><a href="#cb5-141" aria-hidden="true" tabindex="-1"></a>    <span class="fu">aes</span>(</span>
<span id="cb5-142"><a href="#cb5-142" aria-hidden="true" tabindex="-1"></a>      <span class="at">x =</span> boundary_x <span class="sc">-</span> <span class="fl">0.5</span>,</span>
<span id="cb5-143"><a href="#cb5-143" aria-hidden="true" tabindex="-1"></a>      <span class="at">y =</span> <span class="dv">0</span>,</span>
<span id="cb5-144"><a href="#cb5-144" aria-hidden="true" tabindex="-1"></a>      <span class="at">label =</span> <span class="st">"___________"</span></span>
<span id="cb5-145"><a href="#cb5-145" aria-hidden="true" tabindex="-1"></a>    ),</span>
<span id="cb5-146"><a href="#cb5-146" aria-hidden="true" tabindex="-1"></a>    <span class="at">angle =</span> <span class="dv">90</span>,</span>
<span id="cb5-147"><a href="#cb5-147" aria-hidden="true" tabindex="-1"></a>    <span class="at">vjust =</span> .<span class="dv">5</span>,</span>
<span id="cb5-148"><a href="#cb5-148" aria-hidden="true" tabindex="-1"></a>    <span class="at">hjust =</span> <span class="dv">1</span>,</span>
<span id="cb5-149"><a href="#cb5-149" aria-hidden="true" tabindex="-1"></a>    <span class="at">size =</span> <span class="dv">6</span>,</span>
<span id="cb5-150"><a href="#cb5-150" aria-hidden="true" tabindex="-1"></a>    <span class="at">color =</span> <span class="st">"#A9A9A9"</span></span>
<span id="cb5-151"><a href="#cb5-151" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">+</span></span>
<span id="cb5-152"><a href="#cb5-152" aria-hidden="true" tabindex="-1"></a>  <span class="fu">geom_rect</span>(</span>
<span id="cb5-153"><a href="#cb5-153" aria-hidden="true" tabindex="-1"></a>    <span class="fu">aes</span>(</span>
<span id="cb5-154"><a href="#cb5-154" aria-hidden="true" tabindex="-1"></a>      <span class="at">xmin =</span> <span class="fu">as.numeric</span>(xlabel) <span class="sc">-</span> <span class="fl">0.4</span>,</span>
<span id="cb5-155"><a href="#cb5-155" aria-hidden="true" tabindex="-1"></a>      <span class="at">xmax =</span> <span class="fu">as.numeric</span>(xlabel) <span class="sc">+</span> <span class="fl">0.4</span>,</span>
<span id="cb5-156"><a href="#cb5-156" aria-hidden="true" tabindex="-1"></a>      <span class="at">ymin =</span> ymin,</span>
<span id="cb5-157"><a href="#cb5-157" aria-hidden="true" tabindex="-1"></a>      <span class="at">ymax =</span> ymax,</span>
<span id="cb5-158"><a href="#cb5-158" aria-hidden="true" tabindex="-1"></a>      <span class="at">fill =</span> sector</span>
<span id="cb5-159"><a href="#cb5-159" aria-hidden="true" tabindex="-1"></a>    ),</span>
<span id="cb5-160"><a href="#cb5-160" aria-hidden="true" tabindex="-1"></a>    <span class="at">color =</span> <span class="cn">NA</span></span>
<span id="cb5-161"><a href="#cb5-161" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">+</span></span>
<span id="cb5-162"><a href="#cb5-162" aria-hidden="true" tabindex="-1"></a>  <span class="fu">scale_x_continuous</span>(</span>
<span id="cb5-163"><a href="#cb5-163" aria-hidden="true" tabindex="-1"></a>    <span class="at">breaks =</span> <span class="fu">seq_along</span>(<span class="fu">levels</span>(df<span class="sc">$</span>xlabel)),</span>
<span id="cb5-164"><a href="#cb5-164" aria-hidden="true" tabindex="-1"></a>    <span class="at">labels =</span> df <span class="sc">|&gt;</span> <span class="fu">distinct</span>(xlabel, country) <span class="sc">|&gt;</span> <span class="fu">pull</span>(country)</span>
<span id="cb5-165"><a href="#cb5-165" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">+</span></span>
<span id="cb5-166"><a href="#cb5-166" aria-hidden="true" tabindex="-1"></a>  <span class="fu">scale_fill_manual</span>(<span class="at">values =</span> sector_colors) <span class="sc">+</span></span>
<span id="cb5-167"><a href="#cb5-167" aria-hidden="true" tabindex="-1"></a>  <span class="fu">guides</span>(<span class="at">fill =</span> <span class="fu">guide_legend</span>(<span class="at">nrow =</span> <span class="dv">2</span>, <span class="at">byrow =</span> <span class="cn">TRUE</span>)) <span class="sc">+</span></span>
<span id="cb5-168"><a href="#cb5-168" aria-hidden="true" tabindex="-1"></a>  <span class="fu">scale_y_continuous</span>(<span class="at">expand =</span> <span class="fu">c</span>(<span class="dv">0</span>,<span class="dv">0</span>), <span class="at">breaks =</span> <span class="fu">seq</span>(<span class="dv">0</span>,<span class="dv">8</span>,<span class="dv">1</span>), <span class="at">limits =</span> <span class="fu">c</span>(<span class="dv">0</span>,<span class="dv">8</span>)) <span class="sc">+</span></span>
<span id="cb5-169"><a href="#cb5-169" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_cartesian</span>(<span class="at">expand =</span> <span class="cn">FALSE</span>) <span class="sc">+</span></span>
<span id="cb5-170"><a href="#cb5-170" aria-hidden="true" tabindex="-1"></a>  <span class="fu">labs</span>(</span>
<span id="cb5-171"><a href="#cb5-171" aria-hidden="true" tabindex="-1"></a>    <span class="at">title =</span> <span class="st">"Russian hybrid-warfare activity by</span><span class="sc">\n</span><span class="st">country and year, January 2018–June 2025"</span>,</span>
<span id="cb5-172"><a href="#cb5-172" aria-hidden="true" tabindex="-1"></a>    <span class="at">x =</span> <span class="cn">NULL</span>, <span class="at">y =</span> <span class="cn">NULL</span>, <span class="at">fill =</span> <span class="cn">NULL</span></span>
<span id="cb5-173"><a href="#cb5-173" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">+</span></span>
<span id="cb5-174"><a href="#cb5-174" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme_minimal</span>(<span class="at">base_size =</span> <span class="dv">13</span>) <span class="sc">+</span></span>
<span id="cb5-175"><a href="#cb5-175" aria-hidden="true" tabindex="-1"></a>  <span class="fu">theme</span>(</span>
<span id="cb5-176"><a href="#cb5-176" aria-hidden="true" tabindex="-1"></a>    <span class="at">plot.title =</span> <span class="fu">element_text</span>(<span class="at">face =</span> <span class="st">"bold"</span>, <span class="at">size =</span> <span class="dv">20</span>, <span class="at">hjust =</span> <span class="fl">0.5</span>, <span class="at">margin =</span> <span class="fu">margin</span>(<span class="at">b =</span> <span class="dv">8</span>)),</span>
<span id="cb5-177"><a href="#cb5-177" aria-hidden="true" tabindex="-1"></a>    <span class="at">axis.text.x =</span> <span class="fu">element_text</span>(</span>
<span id="cb5-178"><a href="#cb5-178" aria-hidden="true" tabindex="-1"></a>      <span class="at">color =</span> <span class="st">"black"</span>,</span>
<span id="cb5-179"><a href="#cb5-179" aria-hidden="true" tabindex="-1"></a>      <span class="at">size =</span> <span class="dv">9</span>,</span>
<span id="cb5-180"><a href="#cb5-180" aria-hidden="true" tabindex="-1"></a>      <span class="at">angle =</span> <span class="dv">90</span>,</span>
<span id="cb5-181"><a href="#cb5-181" aria-hidden="true" tabindex="-1"></a>      <span class="at">hjust =</span> <span class="dv">1</span>,</span>
<span id="cb5-182"><a href="#cb5-182" aria-hidden="true" tabindex="-1"></a>      <span class="at">vjust =</span> <span class="fl">0.5</span></span>
<span id="cb5-183"><a href="#cb5-183" aria-hidden="true" tabindex="-1"></a>    ),</span>
<span id="cb5-184"><a href="#cb5-184" aria-hidden="true" tabindex="-1"></a>    <span class="at">plot.margin =</span> <span class="fu">margin</span>(<span class="dv">30</span>, <span class="dv">20</span>, <span class="dv">40</span>, <span class="dv">20</span>),</span>
<span id="cb5-185"><a href="#cb5-185" aria-hidden="true" tabindex="-1"></a>    <span class="at">axis.text.y =</span> <span class="fu">element_text</span>(<span class="at">size =</span> <span class="dv">10</span>, <span class="at">color =</span> <span class="st">"grey30"</span>),</span>
<span id="cb5-186"><a href="#cb5-186" aria-hidden="true" tabindex="-1"></a>    <span class="at">panel.grid.major.x =</span> <span class="fu">element_blank</span>(),</span>
<span id="cb5-187"><a href="#cb5-187" aria-hidden="true" tabindex="-1"></a>    <span class="at">panel.grid.minor =</span> <span class="fu">element_blank</span>(),</span>
<span id="cb5-188"><a href="#cb5-188" aria-hidden="true" tabindex="-1"></a>    <span class="at">panel.grid.major.y =</span> <span class="fu">element_line</span>(<span class="at">color =</span> <span class="st">"grey90"</span>),</span>
<span id="cb5-189"><a href="#cb5-189" aria-hidden="true" tabindex="-1"></a>    <span class="at">legend.position =</span> <span class="st">"bottom"</span>,</span>
<span id="cb5-190"><a href="#cb5-190" aria-hidden="true" tabindex="-1"></a>    <span class="at">legend.box =</span> <span class="st">"horizontal"</span>,</span>
<span id="cb5-191"><a href="#cb5-191" aria-hidden="true" tabindex="-1"></a>    <span class="at">legend.text =</span> <span class="fu">element_text</span>(<span class="at">size =</span> <span class="dv">10</span>),</span>
<span id="cb5-192"><a href="#cb5-192" aria-hidden="true" tabindex="-1"></a>    <span class="at">legend.spacing.x =</span> <span class="fu">unit</span>(<span class="fl">0.50</span>, <span class="st">"cm"</span>),</span>
<span id="cb5-193"><a href="#cb5-193" aria-hidden="true" tabindex="-1"></a>    <span class="at">legend.margin =</span> <span class="fu">margin</span>(<span class="at">t =</span> <span class="dv">10</span>),</span>
<span id="cb5-194"><a href="#cb5-194" aria-hidden="true" tabindex="-1"></a>    <span class="at">panel.spacing =</span> <span class="fu">unit</span>(<span class="dv">2</span>, <span class="st">"lines"</span>)</span>
<span id="cb5-195"><a href="#cb5-195" aria-hidden="true" tabindex="-1"></a>  ) <span class="sc">+</span></span>
<span id="cb5-196"><a href="#cb5-196" aria-hidden="true" tabindex="-1"></a>  <span class="fu">coord_cartesian</span>(<span class="at">clip =</span> <span class="st">"off"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>Coordinate system already present.
ℹ Adding new coordinate system, which will replace the existing one.</code></pre>
</div>
<div class="cell-output-display">
<div class="quarto-figure quarto-figure-center">
<figure class="figure">
<p><img src="replicationproject_files/figure-html/unnamed-chunk-1-1.png" class="img-fluid quarto-figure quarto-figure-center figure-img" style="width:100.0%"></p>
</figure>
</div>
</div>
</div>
</section>
<section id="my-replication-1" class="level2">
<h2 class="anchored" data-anchor-id="my-replication-1">My Replication</h2>
<p><img src="rep.png" width="500"></p>
</section>
<section id="original-graph" class="level2">
<h2 class="anchored" data-anchor-id="original-graph">Original Graph</h2>
<p><img src="Russian hybrid warfare activity.png" width="500"></p>
</section>

</main>
<!-- /main column -->
<script id="quarto-html-after-body" type="application/javascript">
window.document.addEventListener("DOMContentLoaded", function (event) {
  const toggleBodyColorMode = (bsSheetEl) => {
    const mode = bsSheetEl.getAttribute("data-mode");
    const bodyEl = window.document.querySelector("body");
    if (mode === "dark") {
      bodyEl.classList.add("quarto-dark");
      bodyEl.classList.remove("quarto-light");
    } else {
      bodyEl.classList.add("quarto-light");
      bodyEl.classList.remove("quarto-dark");
    }
  }
  const toggleBodyColorPrimary = () => {
    const bsSheetEl = window.document.querySelector("link#quarto-bootstrap");
    if (bsSheetEl) {
      toggleBodyColorMode(bsSheetEl);
    }
  }
  toggleBodyColorPrimary();  
  const icon = "";
  const anchorJS = new window.AnchorJS();
  anchorJS.options = {
    placement: 'right',
    icon: icon
  };
  anchorJS.add('.anchored');
  const isCodeAnnotation = (el) => {
    for (const clz of el.classList) {
      if (clz.startsWith('code-annotation-')) {                     
        return true;
      }
    }
    return false;
  }
  const onCopySuccess = function(e) {
    // button target
    const button = e.trigger;
    // don't keep focus
    button.blur();
    // flash "checked"
    button.classList.add('code-copy-button-checked');
    var currentTitle = button.getAttribute("title");
    button.setAttribute("title", "Copied!");
    let tooltip;
    if (window.bootstrap) {
      button.setAttribute("data-bs-toggle", "tooltip");
      button.setAttribute("data-bs-placement", "left");
      button.setAttribute("data-bs-title", "Copied!");
      tooltip = new bootstrap.Tooltip(button, 
        { trigger: "manual", 
          customClass: "code-copy-button-tooltip",
          offset: [0, -8]});
      tooltip.show();    
    }
    setTimeout(function() {
      if (tooltip) {
        tooltip.hide();
        button.removeAttribute("data-bs-title");
        button.removeAttribute("data-bs-toggle");
        button.removeAttribute("data-bs-placement");
      }
      button.setAttribute("title", currentTitle);
      button.classList.remove('code-copy-button-checked');
    }, 1000);
    // clear code selection
    e.clearSelection();
  }
  const getTextToCopy = function(trigger) {
      const codeEl = trigger.previousElementSibling.cloneNode(true);
      for (const childEl of codeEl.children) {
        if (isCodeAnnotation(childEl)) {
          childEl.remove();
        }
      }
      return codeEl.innerText;
  }
  const clipboard = new window.ClipboardJS('.code-copy-button:not([data-in-quarto-modal])', {
    text: getTextToCopy
  });
  clipboard.on('success', onCopySuccess);
  if (window.document.getElementById('quarto-embedded-source-code-modal')) {
    const clipboardModal = new window.ClipboardJS('.code-copy-button[data-in-quarto-modal]', {
      text: getTextToCopy,
      container: window.document.getElementById('quarto-embedded-source-code-modal')
    });
    clipboardModal.on('success', onCopySuccess);
  }
    var localhostRegex = new RegExp(/^(?:http|https):\/\/localhost\:?[0-9]*\//);
    var mailtoRegex = new RegExp(/^mailto:/);
      var filterRegex = new RegExp('/' + window.location.host + '/');
    var isInternal = (href) => {
        return filterRegex.test(href) || localhostRegex.test(href) || mailtoRegex.test(href);
    }
    // Inspect non-navigation links and adorn them if external
 	var links = window.document.querySelectorAll('a[href]:not(.nav-link):not(.navbar-brand):not(.toc-action):not(.sidebar-link):not(.sidebar-item-toggle):not(.pagination-link):not(.no-external):not([aria-hidden]):not(.dropdown-item):not(.quarto-navigation-tool):not(.about-link)');
    for (var i=0; i<links.length; i++) {
      const link = links[i];
      if (!isInternal(link.href)) {
        // undo the damage that might have been done by quarto-nav.js in the case of
        // links that we want to consider external
        if (link.dataset.originalHref !== undefined) {
          link.href = link.dataset.originalHref;
        }
      }
    }
  function tippyHover(el, contentFn, onTriggerFn, onUntriggerFn) {
    const config = {
      allowHTML: true,
      maxWidth: 500,
      delay: 100,
      arrow: false,
      appendTo: function(el) {
          return el.parentElement;
      },
      interactive: true,
      interactiveBorder: 10,
      theme: 'quarto',
      placement: 'bottom-start',
    };
    if (contentFn) {
      config.content = contentFn;
    }
    if (onTriggerFn) {
      config.onTrigger = onTriggerFn;
    }
    if (onUntriggerFn) {
      config.onUntrigger = onUntriggerFn;
    }
    window.tippy(el, config); 
  }
  const noterefs = window.document.querySelectorAll('a[role="doc-noteref"]');
  for (var i=0; i<noterefs.length; i++) {
    const ref = noterefs[i];
    tippyHover(ref, function() {
      // use id or data attribute instead here
      let href = ref.getAttribute('data-footnote-href') || ref.getAttribute('href');
      try { href = new URL(href).hash; } catch {}
      const id = href.replace(/^#\/?/, "");
      const note = window.document.getElementById(id);
      if (note) {
        return note.innerHTML;
      } else {
        return "";
      }
    });
  }
  const xrefs = window.document.querySelectorAll('a.quarto-xref');
  const processXRef = (id, note) => {
    // Strip column container classes
    const stripColumnClz = (el) => {
      el.classList.remove("page-full", "page-columns");
      if (el.children) {
        for (const child of el.children) {
          stripColumnClz(child);
        }
      }
    }
    stripColumnClz(note)
    if (id === null || id.startsWith('sec-')) {
      // Special case sections, only their first couple elements
      const container = document.createElement("div");
      if (note.children && note.children.length > 2) {
        container.appendChild(note.children[0].cloneNode(true));
        for (let i = 1; i < note.children.length; i++) {
          const child = note.children[i];
          if (child.tagName === "P" && child.innerText === "") {
            continue;
          } else {
            container.appendChild(child.cloneNode(true));
            break;
          }
        }
        if (window.Quarto?.typesetMath) {
          window.Quarto.typesetMath(container);
        }
        return container.innerHTML
      } else {
        if (window.Quarto?.typesetMath) {
          window.Quarto.typesetMath(note);
        }
        return note.innerHTML;
      }
    } else {
      // Remove any anchor links if they are present
      const anchorLink = note.querySelector('a.anchorjs-link');
      if (anchorLink) {
        anchorLink.remove();
      }
      if (window.Quarto?.typesetMath) {
        window.Quarto.typesetMath(note);
      }
      if (note.classList.contains("callout")) {
        return note.outerHTML;
      } else {
        return note.innerHTML;
      }
    }
  }
  for (var i=0; i<xrefs.length; i++) {
    const xref = xrefs[i];
    tippyHover(xref, undefined, function(instance) {
      instance.disable();
      let url = xref.getAttribute('href');
      let hash = undefined; 
      if (url.startsWith('#')) {
        hash = url;
      } else {
        try { hash = new URL(url).hash; } catch {}
      }
      if (hash) {
        const id = hash.replace(/^#\/?/, "");
        const note = window.document.getElementById(id);
        if (note !== null) {
          try {
            const html = processXRef(id, note.cloneNode(true));
            instance.setContent(html);
          } finally {
            instance.enable();
            instance.show();
          }
        } else {
          // See if we can fetch this
          fetch(url.split('#')[0])
          .then(res => res.text())
          .then(html => {
            const parser = new DOMParser();
            const htmlDoc = parser.parseFromString(html, "text/html");
            const note = htmlDoc.getElementById(id);
            if (note !== null) {
              const html = processXRef(id, note);
              instance.setContent(html);
            } 
          }).finally(() => {
            instance.enable();
            instance.show();
          });
        }
      } else {
        // See if we can fetch a full url (with no hash to target)
        // This is a special case and we should probably do some content thinning / targeting
        fetch(url)
        .then(res => res.text())
        .then(html => {
          const parser = new DOMParser();
          const htmlDoc = parser.parseFromString(html, "text/html");
          const note = htmlDoc.querySelector('main.content');
          if (note !== null) {
            // This should only happen for chapter cross references
            // (since there is no id in the URL)
            // remove the first header
            if (note.children.length > 0 && note.children[0].tagName === "HEADER") {
              note.children[0].remove();
            }
            const html = processXRef(null, note);
            instance.setContent(html);
          } 
        }).finally(() => {
          instance.enable();
          instance.show();
        });
      }
    }, function(instance) {
    });
  }
      let selectedAnnoteEl;
      const selectorForAnnotation = ( cell, annotation) => {
        let cellAttr = 'data-code-cell="' + cell + '"';
        let lineAttr = 'data-code-annotation="' +  annotation + '"';
        const selector = 'span[' + cellAttr + '][' + lineAttr + ']';
        return selector;
      }
      const selectCodeLines = (annoteEl) => {
        const doc = window.document;
        const targetCell = annoteEl.getAttribute("data-target-cell");
        const targetAnnotation = annoteEl.getAttribute("data-target-annotation");
        const annoteSpan = window.document.querySelector(selectorForAnnotation(targetCell, targetAnnotation));
        const lines = annoteSpan.getAttribute("data-code-lines").split(",");
        const lineIds = lines.map((line) => {
          return targetCell + "-" + line;
        })
        let top = null;
        let height = null;
        let parent = null;
        if (lineIds.length > 0) {
            //compute the position of the single el (top and bottom and make a div)
            const el = window.document.getElementById(lineIds[0]);
            top = el.offsetTop;
            height = el.offsetHeight;
            parent = el.parentElement.parentElement;
          if (lineIds.length > 1) {
            const lastEl = window.document.getElementById(lineIds[lineIds.length - 1]);
            const bottom = lastEl.offsetTop + lastEl.offsetHeight;
            height = bottom - top;
          }
          if (top !== null && height !== null && parent !== null) {
            // cook up a div (if necessary) and position it 
            let div = window.document.getElementById("code-annotation-line-highlight");
            if (div === null) {
              div = window.document.createElement("div");
              div.setAttribute("id", "code-annotation-line-highlight");
              div.style.position = 'absolute';
              parent.appendChild(div);
            }
            div.style.top = top - 2 + "px";
            div.style.height = height + 4 + "px";
            div.style.left = 0;
            let gutterDiv = window.document.getElementById("code-annotation-line-highlight-gutter");
            if (gutterDiv === null) {
              gutterDiv = window.document.createElement("div");
              gutterDiv.setAttribute("id", "code-annotation-line-highlight-gutter");
              gutterDiv.style.position = 'absolute';
              const codeCell = window.document.getElementById(targetCell);
              const gutter = codeCell.querySelector('.code-annotation-gutter');
              gutter.appendChild(gutterDiv);
            }
            gutterDiv.style.top = top - 2 + "px";
            gutterDiv.style.height = height + 4 + "px";
          }
          selectedAnnoteEl = annoteEl;
        }
      };
      const unselectCodeLines = () => {
        const elementsIds = ["code-annotation-line-highlight", "code-annotation-line-highlight-gutter"];
        elementsIds.forEach((elId) => {
          const div = window.document.getElementById(elId);
          if (div) {
            div.remove();
          }
        });
        selectedAnnoteEl = undefined;
      };
        // Handle positioning of the toggle
    window.addEventListener(
      "resize",
      throttle(() => {
        elRect = undefined;
        if (selectedAnnoteEl) {
          selectCodeLines(selectedAnnoteEl);
        }
      }, 10)
    );
    function throttle(fn, ms) {
    let throttle = false;
    let timer;
      return (...args) => {
        if(!throttle) { // first call gets through
            fn.apply(this, args);
            throttle = true;
        } else { // all the others get throttled
            if(timer) clearTimeout(timer); // cancel #2
            timer = setTimeout(() => {
              fn.apply(this, args);
              timer = throttle = false;
            }, ms);
        }
      };
    }
      // Attach click handler to the DT
      const annoteDls = window.document.querySelectorAll('dt[data-target-cell]');
      for (const annoteDlNode of annoteDls) {
        annoteDlNode.addEventListener('click', (event) => {
          const clickedEl = event.target;
          if (clickedEl !== selectedAnnoteEl) {
            unselectCodeLines();
            const activeEl = window.document.querySelector('dt[data-target-cell].code-annotation-active');
            if (activeEl) {
              activeEl.classList.remove('code-annotation-active');
            }
            selectCodeLines(clickedEl);
            clickedEl.classList.add('code-annotation-active');
          } else {
            // Unselect the line
            unselectCodeLines();
            clickedEl.classList.remove('code-annotation-active');
          }
        });
      }
  const findCites = (el) => {
    const parentEl = el.parentElement;
    if (parentEl) {
      const cites = parentEl.dataset.cites;
      if (cites) {
        return {
          el,
          cites: cites.split(' ')
        };
      } else {
        return findCites(el.parentElement)
      }
    } else {
      return undefined;
    }
  };
  var bibliorefs = window.document.querySelectorAll('a[role="doc-biblioref"]');
  for (var i=0; i<bibliorefs.length; i++) {
    const ref = bibliorefs[i];
    const citeInfo = findCites(ref);
    if (citeInfo) {
      tippyHover(citeInfo.el, function() {
        var popup = window.document.createElement('div');
        citeInfo.cites.forEach(function(cite) {
          var citeDiv = window.document.createElement('div');
          citeDiv.classList.add('hanging-indent');
          citeDiv.classList.add('csl-entry');
          var biblioDiv = window.document.getElementById('ref-' + cite);
          if (biblioDiv) {
            citeDiv.innerHTML = biblioDiv.innerHTML;
          }
          popup.appendChild(citeDiv);
        });
        return popup.innerHTML;
      });
    }
  }
});
</script>
</div> <!-- /content -->




</body></html>
