---
marp: true
title: "Presentation Title"
footer: "Author"
math: mathjax
paginate: true
size: 16:9
---

<style>
h1 {
  color: #39c5bb;
  text-align: center;
  display: flex;
  align-items: center;
  gap: 16px;
}
h1::before, h1::after {
  content: "";
  flex: 1;
  height: 8px;
  background: #39c5bb;
}
h2 {
  color: #66ccff;
  border-bottom: 4px solid #66ccff;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: white;
  z-index: 100;
  padding: 10px 60px;
  margin: 0;
}
h3 {
  color: #fff;
  background: #d93a49;
  display: block;
  padding: 5px 20px;
}
fieldset p { margin: 0; }
div p { margin: 0; }
fieldset {
  display: flex;
  flex-direction: column;
  justify-content: center;
  line-height: 1.5;
}
legend {
  font-weight: bold;
  padding: 0 6px;
}
</style>

<!-- Translate all audience-facing placeholders into the selected presentation language. -->
<!-- Keep legend text plain. Put Markdown content on separate lines with blank lines between it and surrounding HTML tags. -->
<!-- Follow references/latex-style.md for every mathematical expression. -->
<!-- If the agenda is too long for one vertical list, wrap the list in <div style="column-count:2; column-gap:36px;">. -->

<div style="margin-bottom:16px; color:#114514; font-weight:bold; font-size:1.4em; border-bottom:2px solid #191981; padding-bottom:8px;">Agenda</div>

<ul>
<li style="color:#39c5bb;">General Templates
<ul>
<li style="color:#66ccff;">Balanced two-column cards</li>
<li style="color:#66ccff;">Asymmetric three-card composition</li>
<li style="color:#66ccff;">Horizontal process diagram</li>
<li style="color:#66ccff;">One-over-three card layout</li>
<li style="color:#66ccff;">Stacked labeled information rows</li>
<li style="color:#66ccff;">Citation and annotation elements</li>
</ul>
</li>
<li style="color:#39c5bb;">Special Templates
<ul>
<li style="color:#66ccff;">Framework and dependency structures</li>
<li style="color:#66ccff;">Stages and compound processes</li>
<li style="color:#66ccff;">Contrasts and method landscapes</li>
</ul>
</li>
</ul>

---

# General Templates

---

## Balanced Two-Column Cards

<br>

<div style="display:grid; grid-template-columns:1fr 1fr; gap:20px; margin-top:10px;">

<fieldset style="border:2px solid #3b82f6; border-radius:8px; padding:14px; background:linear-gradient(to bottom,#ffffff,#dbeafe 61.8%);">
  <legend style="font-weight:bold; color:#1e40af; padding:0 6px;">Concept A</legend>
  <div style="font-size:0.85em; color:#374151; line-height:1.9;">

- Key point
- Key point

  </div>
</fieldset>

<fieldset style="border:2px solid #d93a49; border-radius:8px; padding:14px; background:linear-gradient(to bottom,#ffffff,#fff1f2 61.8%);">
  <legend style="font-weight:bold; color:#7f0000; padding:0 6px;">Concept B</legend>
  <div style="font-size:0.85em; color:#374151; line-height:1.9;">

- Key point
- Key point

  </div>
</fieldset>

</div>

---

## Asymmetric Three-Card Composition

<div style="display:grid; grid-template-columns:1.15fr 1fr; gap:16px; margin-top:30px; min-height:360px;">

<fieldset style="border:2px solid #f59e0b; border-radius:8px; padding:16px; background:linear-gradient(to bottom,#ffffff,#fef3c7 61.8%);">
  <legend style="font-weight:bold; color:#92400e; padding:0 6px;">Euler identity</legend>
  <div style="font-size:0.88em; color:#374151; line-height:1.8; text-align:center;">

$$
\mathrm{e}^{\pi\mathrm{i}}+1=0
$$

A compact example connecting fundamental constants in one relation.

  </div>
</fieldset>

<div style="display:grid; grid-template-rows:1fr 1fr; gap:16px;">

<fieldset style="border:2px solid #8b5cf6; border-radius:8px; padding:12px; background:linear-gradient(to bottom,#ffffff,#ede9fe 61.8%);">
  <legend style="font-weight:bold; color:#5b21b6; padding:0 6px;">Interpretation</legend>
  <div style="font-size:0.8em; color:#374151; line-height:1.7;">

Use this card for assumptions, physical interpretation, or supporting context.

  </div>
</fieldset>

<fieldset style="border:2px solid #10b981; border-radius:8px; padding:12px; background:linear-gradient(to bottom,#ffffff,#d1fae5 61.8%);">
  <legend style="font-weight:bold; color:#065f46; padding:0 6px;">Significance</legend>
  <div style="font-size:0.8em; color:#374151; line-height:1.7;">

Use this card for the result, implication, or next action.

  </div>
</fieldset>

</div>

</div>

---

## Horizontal Process Diagram

<!-- Give each node one dominant hue with a local gradient. Blend each arrow between the adjacent endpoint colors. -->
<div style="display:flex; align-items:center; justify-content:center; gap:8px; margin-top:30px; font-size:0.72em; flex-wrap:nowrap;">

<div style="background:linear-gradient(135deg,#667eea,#764ba2); color:white; padding:12px 16px; border-radius:8px; font-weight:bold; text-align:center; min-width:105px;">

Step 1

</div>

<div style="font-size:1.7em; font-weight:bold; background:linear-gradient(90deg,#764ba2,#f093fb); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">

→

</div>

<div style="background:linear-gradient(135deg,#f093fb,#f5576c); color:white; padding:12px 16px; border-radius:8px; font-weight:bold; text-align:center; min-width:105px;">

Step 2

</div>

<div style="font-size:1.7em; font-weight:bold; background:linear-gradient(90deg,#f5576c,#4facfe); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">

→

</div>

<div style="background:linear-gradient(135deg,#4facfe,#00f2fe); color:white; padding:12px 16px; border-radius:8px; font-weight:bold; text-align:center; min-width:105px;">

Step 3

</div>

<div style="font-size:1.7em; font-weight:bold; background:linear-gradient(90deg,#00f2fe,#43e97b); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">

→

</div>

<div style="background:linear-gradient(135deg,#43e97b,#38f9d7); color:white; padding:12px 16px; border-radius:8px; font-weight:bold; text-align:center; min-width:105px;">

Step 4

</div>

<div style="font-size:1.7em; font-weight:bold; background:linear-gradient(90deg,#38f9d7,#f97316); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">

→

</div>

<div style="background:linear-gradient(135deg,#f97316,#fbbf24); color:white; padding:12px 16px; border-radius:8px; font-weight:bold; text-align:center; min-width:105px;">

Step 5

</div>

</div>

---

## One-over-Three Card Layout

<fieldset style="border:2px solid #3b82f6; border-radius:8px; padding:10px 16px; background:linear-gradient(to bottom,#ffffff,#dbeafe 61.8%); margin-top:24px;">
  <legend style="font-weight:bold; color:#1e40af; padding:0 6px;">Top card</legend>
  <div style="font-size:0.82em; color:#374151; text-align:center;">

Primary content

  </div>
</fieldset>

<div style="display:grid; grid-template-columns:1fr 1fr 1fr; gap:14px; margin-top:18px;">

<fieldset style="border:2px solid #10b981; border-radius:8px; padding:10px; background:linear-gradient(to bottom,#ffffff,#d1fae5 61.8%);">
  <legend style="font-weight:bold; color:#065f46; padding:0 6px;">Lower card A</legend>
  <div style="font-size:0.8em; color:#374151; text-align:center; line-height:1.5;">

<div>Secondary content</div>
<div>Supporting detail</div>

  </div>
</fieldset>

<fieldset style="border:2px solid #8b5cf6; border-radius:8px; padding:10px; background:linear-gradient(to bottom,#ffffff,#ede9fe 61.8%);">
  <legend style="font-weight:bold; color:#5b21b6; padding:0 6px;">Lower card B</legend>
  <div style="font-size:0.8em; color:#374151; text-align:center;line-height:1.5;">

<div>Secondary content</div>
<div>Supporting detail</div>

  </div>
</fieldset>

<fieldset style="border:2px solid #ec4899; border-radius:8px; padding:10px; background:linear-gradient(to bottom,#ffffff,#fce7f3 61.8%);">
  <legend style="font-weight:bold; color:#9f1239; padding:0 6px;">Lower card C</legend>
  <div style="font-size:0.8em; color:#374151; text-align:center; line-height:1.5;">

<div>Secondary content</div>
<div>Supporting detail</div>

  </div>
</fieldset>

</div>

---

## Stacked Labeled Information Rows

<div style="display:flex; flex-direction:column; gap:12px; margin-top:30px;">

<div  style="display:flex; align-items:center; gap:14px; padding:10px 16px; background:#fff7ed; border-left:4px solid #ea580c; border-radius:4px;">
  <div style="font-weight:bold; color:#c2410c; min-width:6.5em; font-size:0.83em;">Label A</div>
  <div style="color:#374151; font-size:0.8em; line-height:1.5; flex:1;">

Description for item A.

  </div>
</div>

<div  style="display:flex; align-items:center; gap:14px; padding:10px 16px; background:#fdf2f8; border-left:4px solid #db2777; border-radius:4px;">
  <div style="font-weight:bold; color:#be185d; min-width:6.5em; font-size:0.83em;">Label B</div>
  <div style="color:#374151; font-size:0.8em; line-height:1.5; flex:1;">

Description for item B.

  </div>
</div>

<div  style="display:flex; align-items:center; gap:14px; padding:10px 16px; background:#f5f3ff; border-left:4px solid #7c3aed; border-radius:4px;">
  <div style="font-weight:bold; color:#6d28d9; min-width:6.5em; font-size:0.83em;">Label C</div>
  <div style="color:#374151; font-size:0.8em; line-height:1.5; flex:1;">

Description for item C.

  </div>
</div>

<div  style="display:flex; align-items:center; gap:14px; padding:10px 16px; background:#fffbeb; border-left:4px solid #d97706; border-radius:4px;">

<div style="font-weight:bold; color:#b45309; min-width:6.5em; font-size:0.83em;">Label D</div>
<div style="color:#374151; font-size:0.8em; line-height:1.5; flex:1;">

Description for item D.

</div>

</div>

</div>

---

## Citation and Annotation Elements

<div style="position:fixed; top:0; right:0; padding:5px; color:black; font-family:'Times New Roman'; font-style:italic; z-index:999; line-height:1.0; text-align:right;">

Author et al. Journal Volume, Page (Year).
Author et al. Journal Volume, Page (Year).

</div>

<div style="display:flex; align-items:center; gap:24px; margin-top:34px;">

<fieldset style="order:2; flex:0 0 29%; border:2px solid #f59e0b; border-radius:8px; padding:12px 14px; background:linear-gradient(to bottom,#ffffff,#fef3c7 61.8%);">
  <legend style="font-weight:bold; color:#92400e; padding:0 6px;">Interpretation</legend>
  <div style="font-size:0.78em; color:#374151; line-height:1.5;">

Use this area for the presenter's interpretation, the physical meaning of the figure, important trends, limitations, or the connection to the current work.

  </div>
</fieldset>

<div style="order:1; flex:1; min-width:0;">

<div style="text-align:center;">

<img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA4MDAgMzYwIj48ZGVmcz48bGluZWFyR3JhZGllbnQgaWQ9ImJnIiB4MT0iMCIgeDI9IjEiIHkxPSIwIiB5Mj0iMSI+PHN0b3Agc3RvcC1jb2xvcj0iI2VmZjZmZiIvPjxzdG9wIG9mZnNldD0iMSIgc3RvcC1jb2xvcj0iI2VjZmRmNSIvPjwvbGluZWFyR3JhZGllbnQ+PGxpbmVhckdyYWRpZW50IGlkPSJsaW5lIiB4MT0iMCIgeDI9IjEiPjxzdG9wIHN0b3AtY29sb3I9IiMzYjgyZjYiLz48c3RvcCBvZmZzZXQ9Ii41IiBzdG9wLWNvbG9yPSIjOGI1Y2Y2Ii8+PHN0b3Agb2Zmc2V0PSIxIiBzdG9wLWNvbG9yPSIjMTBiOTgxIi8+PC9saW5lYXJHcmFkaWVudD48L2RlZnM+PHJlY3Qgd2lkdGg9IjgwMCIgaGVpZ2h0PSIzNjAiIHJ4PSIxOCIgZmlsbD0idXJsKCNiZykiLz48ZyBzdHJva2U9IiNjYmQ1ZTEiIHN0cm9rZS13aWR0aD0iMiIgb3BhY2l0eT0iLjciPjxwYXRoIGQ9Ik03MCA1NVYzMDBINzQ1Ii8+PHBhdGggZD0iTTcwIDI0MEg3NDVNNzAgMTgwSDc0NU03MCAxMjBINzQ1Ii8+PC9nPjxwYXRoIGQ9Ik05MCAyNjVDMTc1IDI1MCAyMDUgMjEwIDI4MCAyMjBTMzk1IDE0NSA0NjUgMTY1IDU3NSA4NSA3MTAgMTA1IiBmaWxsPSJub25lIiBzdHJva2U9InVybCgjbGluZSkiIHN0cm9rZS13aWR0aD0iMTIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIvPjxnIGZpbGw9IiNmZmYiIHN0cm9rZS13aWR0aD0iNyI+PGNpcmNsZSBjeD0iOTAiIGN5PSIyNjUiIHI9IjE1IiBzdHJva2U9IiMzYjgyZjYiLz48Y2lyY2xlIGN4PSIyODAiIGN5PSIyMjAiIHI9IjE1IiBzdHJva2U9IiM2MzY2ZjEiLz48Y2lyY2xlIGN4PSI0NjUiIGN5PSIxNjUiIHI9IjE1IiBzdHJva2U9IiM4YjVjZjYiLz48Y2lyY2xlIGN4PSI3MTAiIGN5PSIxMDUiIHI9IjE1IiBzdHJva2U9IiMxMGI5ODEiLz48L2c+PC9zdmc+" alt="Generic figure placeholder" style="display:block; width:68%; max-height:270px; object-fit:contain; margin:0 auto; border-radius:8px; box-shadow:0 3px 12px rgba(15,23,42,0.12);">

</div>

<div style="width:68%; margin:8px auto 0; text-align:left;">

<span style="font-size:small; color:gray; font-style:italic;">

\* Annotation text.

</span>

</div>

</div>

</div>

---

# Special Templates

---

## Directory-Based Task Framework

<div style="margin-top:34px; font-size:0.68em;">

<div style="display:flex; justify-content:center;">

<fieldset style="border:3px solid #39c5bb; border-radius:10px; padding:10px; display:inline-block;">
  <legend style="font-weight:bold; color:#39c5bb; padding:0 8px; font-size:1.3em;">root/</legend>

<div style="display:flex; gap:10px; align-items:stretch;">

<fieldset style="border:2px solid #d93a49; border-radius:8px; padding:6px; display:flex; flex-direction:column;">
  <legend style="font-weight:bold; color:#7f0000; padding:0 6px; font-size:1.1em;">workflow-a/</legend>
  <div style="color:#666; font-size:0.85em; margin-bottom:6px; text-align:center; font-style:italic;">Purpose or condition family</div>

<fieldset style="border:1.5px solid #3b82f6; border-radius:5px; padding:4px 6px; margin-bottom:4px;">
  <legend style="font-weight:bold; color:#1e40af; padding:0 4px; font-size:0.95em;">system-1/</legend>
  <div style="display:flex; gap:4px;">
    <span style="background:#fee2e2; padding:2px 6px; border-radius:3px;">case-1/</span>
    <span style="background:#fee2e2; padding:2px 6px; border-radius:3px;">case-2/</span>
    <span style="background:#fee2e2; padding:2px 6px; border-radius:3px;">case-3/</span>
  </div>
</fieldset>

<fieldset style="border:1.5px solid #3b82f6; border-radius:5px; padding:4px 6px;">
  <legend style="font-weight:bold; color:#1e40af; padding:0 4px; font-size:0.95em;">system-2/</legend>
  <div style="display:flex; gap:4px;">
    <span style="background:#fee2e2; padding:2px 6px; border-radius:3px;">case-1/</span>
    <span style="background:#fee2e2; padding:2px 6px; border-radius:3px;">case-2/</span>
    <span style="background:#fee2e2; padding:2px 6px; border-radius:3px;">case-3/</span>
  </div>
</fieldset>
</fieldset>

<fieldset style="border:2px solid #f97316; border-radius:8px; padding:6px; display:flex; flex-direction:column;">
  <legend style="font-weight:bold; color:#9a3412; padding:0 6px; font-size:1.1em;">workflow-b/</legend>
  <div style="color:#666; font-size:0.85em; margin-bottom:6px; text-align:center; font-style:italic;">Purpose or condition family</div>

<fieldset style="border:1.5px solid #8b5cf6; border-radius:5px; padding:4px 6px; margin-bottom:4px;">
  <legend style="font-weight:bold; color:#5b21b6; padding:0 4px; font-size:0.95em;">system-1/</legend>
  <div style="display:flex; gap:4px; flex-wrap:wrap;">
    <span style="background:#ffedd5; padding:2px 6px; border-radius:3px;">case-1/</span>
    <span style="background:#ffedd5; padding:2px 6px; border-radius:3px;">case-2/</span>
    <span style="background:#ffedd5; padding:2px 6px; border-radius:3px;">case-3/</span>
  </div>
</fieldset>

<fieldset style="border:1.5px solid #8b5cf6; border-radius:5px; padding:4px 6px;">
  <legend style="font-weight:bold; color:#5b21b6; padding:0 4px; font-size:0.95em;">system-2/</legend>
  <div style="display:flex; gap:4px; flex-wrap:wrap;">
    <span style="background:#ffedd5; padding:2px 6px; border-radius:3px;">case-1/</span>
    <span style="background:#ffedd5; padding:2px 6px; border-radius:3px;">case-2/</span>
    <span style="background:#ffedd5; padding:2px 6px; border-radius:3px;">case-3/</span>
  </div>
</fieldset>
</fieldset>

<fieldset style="border:2px solid #eab308; border-radius:8px; padding:6px; display:flex; flex-direction:column;">
  <legend style="font-weight:bold; color:#854d0e; padding:0 6px; font-size:1.1em;">workflow-c/</legend>
  <div style="color:#666; font-size:0.85em; margin-bottom:6px; text-align:center; font-style:italic;">Purpose or condition family</div>

<fieldset style="border:1.5px solid #ec4899; border-radius:5px; padding:4px 6px; margin-bottom:4px;">
  <legend style="font-weight:bold; color:#9f1239; padding:0 4px; font-size:0.95em;">system-1/</legend>
  <div style="display:flex; gap:4px;">
    <span style="background:#fef9c3; padding:2px 6px; border-radius:3px;">run-1/</span>
    <span style="background:#fef9c3; padding:2px 6px; border-radius:3px;">run-2/</span>
    <span style="background:#fef9c3; padding:2px 6px; border-radius:3px;">run-3/</span>
  </div>
</fieldset>

<fieldset style="border:1.5px solid #ec4899; border-radius:5px; padding:4px 6px;">
  <legend style="font-weight:bold; color:#9f1239; padding:0 4px; font-size:0.95em;">system-2/</legend>
  <div style="display:flex; gap:4px;">
    <span style="background:#fef9c3; padding:2px 6px; border-radius:3px;">run-1/</span>
    <span style="background:#fef9c3; padding:2px 6px; border-radius:3px;">run-2/</span>
    <span style="background:#fef9c3; padding:2px 6px; border-radius:3px;">run-3/</span>
  </div>
</fieldset>
</fieldset>

</div>
</fieldset>
</div>

<div style="display:flex; justify-content:center; gap:24px; margin-top:8px;">
  <fieldset style="border:1.5px solid #8b5cf6; border-radius:5px; padding:3px 10px;">
    <legend style="font-weight:bold; color:#5b21b6; padding:0 4px; font-size:1.05em;">Engine A</legend>
    Shared engine, ensemble, and time-step settings
  </fieldset>
  <fieldset style="border:1.5px solid #10b981; border-radius:5px; padding:3px 10px;">
    <legend style="font-weight:bold; color:#065f46; padding:0 4px; font-size:1.05em;">Engine B</legend>
    Shared engine, ensemble, and time-step settings
  </fieldset>
</div>

</div>

---

## Stage with Progress Bar

<div style="margin-top:10px;">

<div style="display:flex; align-items:center; justify-content:space-between; font-size:0.8em; color:#374151; margin-bottom:4px; width:100%;">

<span style="display:block; flex:1 1 33.333%; text-align:left;">

Progress = 0

</span>

<span style="display:block; flex:1 1 33.333%; text-align:center;">

Progress is advancing

</span>

<span style="display:block; flex:1 1 33.333%; text-align:right;">

Progress = 1

</span>

</div>

<div style="height:36px; border-radius:8px; background:linear-gradient(90deg,#3b82f6 0%,#8b5cf6 30%,#ec4899 65%,#f59e0b 100%); position:relative;">
  <div style="position:absolute; left:12px; top:50%; transform:translateY(-50%); color:white; font-weight:bold; font-size:0.8em;">Initial</div>
  <div style="position:absolute; right:12px; top:50%; transform:translateY(-50%); color:white; font-weight:bold; font-size:0.8em;">Final</div>
</div>

</div>

<div style="display:flex; align-items:center; gap:10px; margin-top:30px; justify-content:center; font-size:0.72em;">

<div style="background:linear-gradient(135deg,#3b82f6,#06b6d4); color:white; padding:14px 16px; border-radius:8px; text-align:center; font-weight:bold; min-width:100px;">

Stage 1
<div style="font-weight:normal; font-size:0.8em; margin-top:4px;">Stage 1 note</div>

</div>

<div style="font-size:1.6em; font-weight:bold; background:linear-gradient(90deg,#06b6d4,#8b5cf6); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">

→

</div>

<div style="background:linear-gradient(135deg,#8b5cf6,#a78bfa); color:white; padding:14px 16px; border-radius:8px; text-align:center; font-weight:bold; min-width:100px;">

Stage 2
<div style="font-weight:normal; font-size:0.8em; margin-top:4px;">Stage 2 note</div>

</div>

<div style="font-size:1.6em; font-weight:bold; background:linear-gradient(90deg,#a78bfa,#ec4899); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">

→

</div>

<div style="background:linear-gradient(135deg,#ec4899,#f472b6); color:white; padding:14px 16px; border-radius:8px; text-align:center; font-weight:bold; min-width:100px;">

Stage 3
<div style="font-weight:normal; font-size:0.8em; margin-top:4px;">Stage 3 note</div>

</div>

<div style="font-size:1.6em; font-weight:bold; background:linear-gradient(90deg,#f472b6,#f97316); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">

→

</div>

<div style="background:linear-gradient(135deg,#f97316,#fbbf24); color:white; padding:14px 16px; border-radius:8px; text-align:center; font-weight:bold; min-width:100px;">

Stage 4
<div style="font-weight:normal; font-size:0.8em; margin-top:4px;">Stage 4 note</div>

</div>

</div>

---

## Grouped Serial and Parallel Process

<div style="display:flex; align-items:center; justify-content:center; gap:12px; margin-top:34px; font-size:0.72em;">

<div style="background:linear-gradient(135deg,#10b981,#06b6d4); color:white; padding:14px 18px; border-radius:8px; font-weight:bold;">Input</div>
<div style="font-size:1.7em; font-weight:bold; background:linear-gradient(90deg,#06b6d4,#8b5cf6); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">→</div>

<div style="display:flex; align-items:center; gap:10px; padding:14px; border:3px solid transparent; border-radius:9px; background:linear-gradient(white,white) padding-box,linear-gradient(135deg,#8b5cf6,#ec4899) border-box;">

<div style="background:#ede9fe; color:#5b21b6; padding:10px 14px; border-radius:6px; font-weight:bold;">Serial A</div>
<div style="font-size:1.4em; background:linear-gradient(90deg,#8b5cf6,#ec4899); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">→</div>
<div style="background:#fce7f3; color:#9f1239; padding:10px 14px; border-radius:6px; font-weight:bold;">Serial B</div>

</div>

<div style="font-size:1.7em; font-weight:bold; background:linear-gradient(90deg,#ec4899,#f97316); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">→</div>

<div style="display:flex; flex-direction:column; gap:8px; padding:14px; border:3px solid transparent; border-radius:9px; background:linear-gradient(white,white) padding-box,linear-gradient(135deg,#ef4444,#fbbf24) border-box;">

<div style="background:#fee2e2; color:#991b1b; padding:8px 14px; border-radius:6px; font-weight:bold;">Parallel A</div>
<div style="background:#ffedd5; color:#9a3412; padding:8px 14px; border-radius:6px; font-weight:bold;">Parallel B</div>
<div style="background:#fef3c7; color:#92400e; padding:8px 14px; border-radius:6px; font-weight:bold;">Parallel C</div>

</div>

<div style="font-size:1.7em; font-weight:bold; background:linear-gradient(90deg,#f97316,#30cfd0); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">→</div>
<div style="background:linear-gradient(135deg,#30cfd0,#330867); color:white; padding:14px 18px; border-radius:8px; font-weight:bold;">Output</div>

</div>

---

## Visual Contrast Before the Takeaway

<div style="display:grid; grid-template-columns:minmax(0,1fr) auto minmax(0,1fr); gap:20px; align-items:stretch; margin-top:18px;">

<div style="height:225px; min-width:0; background:#0f172a; border:2px solid #475569; border-radius:8px; overflow:hidden; display:flex; flex-direction:column; box-sizing:border-box;">
  <div style="background:#1e293b; color:#94a3b8; padding:8px 12px; font-size:0.72em; flex:0 0 auto;">Elaborate plan</div>
  <div style="flex:1 1 auto; min-height:0; padding:12px; color:#94a3b8; font-family:monospace; font-size:clamp(0.42em,1.05vw,0.58em); line-height:1.45; overflow:hidden; overflow-wrap:anywhere; word-break:break-word; box-sizing:border-box;">

Layer One
Layer Two
Many future abstractions

  </div>
</div>

<div style="display:flex; align-items:center; justify-content:center; color:#475569; font-size:1.5em; font-weight:bold;">vs</div>

<div style="height:225px; min-width:0; background:#0f172a; border:2px solid #475569; border-radius:8px; overflow:hidden; display:flex; flex-direction:column; box-sizing:border-box;">
  <div style="background:#1e293b; color:#94a3b8; padding:8px 12px; font-size:0.72em; flex:0 0 auto;">Actual state</div>
  <div style="flex:1 1 auto; min-height:0; padding:12px; display:flex; align-items:center; justify-content:center; text-align:center; color:#d93a49; font-size:clamp(1.5em,4vw,3em); line-height:1.05; font-weight:bold; overflow:hidden; overflow-wrap:anywhere; box-sizing:border-box;">Minimal result</div>
</div>

</div>

<fieldset style="margin-top:16px; border:2px solid #d93a49; border-radius:10px; padding:10px 18px; background:linear-gradient(to bottom,#ffffff,#fff1f2 61.8%);">
  <legend style="font-weight:bold; color:#7f0000; padding:0 8px;">Takeaway</legend>
  <div style="color:#374151; font-size:0.84em; text-align:center;">

Explain the lesson after the visual contrast has made the tension obvious.

  </div>
</fieldset>

---

## Multiscale Dependency Ladder

<div style="display:flex; flex-direction:column; align-items:center; gap:6px; margin-top:28px; font-size:0.76em;">

<div style="width:94%; background:linear-gradient(135deg,#fce7f3,#fbcfe8); border:2px solid #ec4899; border-radius:8px; padding:10px; text-align:center; font-weight:bold; color:#9f1239;">Macroscopic outcome</div>
<div style="font-size:1.25em; font-weight:bold; background:linear-gradient(0deg,#8b5cf6,#ec4899); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">↑</div>
<div style="width:82%; background:linear-gradient(135deg,#ede9fe,#ddd6fe); border:2px solid #8b5cf6; border-radius:8px; padding:10px; text-align:center; font-weight:bold; color:#5b21b6;">Emergent behavior</div>
<div style="font-size:1.25em; font-weight:bold; background:linear-gradient(0deg,#3b82f6,#8b5cf6); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">↑</div>
<div style="width:70%; background:linear-gradient(135deg,#dbeafe,#bfdbfe); border:2px solid #3b82f6; border-radius:8px; padding:10px; text-align:center; font-weight:bold; color:#1e40af;">Mesoscopic organization</div>
<div style="font-size:1.25em; font-weight:bold; background:linear-gradient(0deg,#06b6d4,#3b82f6); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">↑</div>
<div style="width:58%; background:linear-gradient(135deg,#cffafe,#a5f3fc); border:2px solid #06b6d4; border-radius:8px; padding:10px; text-align:center; font-weight:bold; color:#0e7490;">Local arrangement</div>
<div style="font-size:1.25em; font-weight:bold; background:linear-gradient(0deg,#10b981,#06b6d4); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">↑</div>
<div style="width:46%; background:linear-gradient(135deg,#d1fae5,#a7f3d0); border:2px solid #10b981; border-radius:8px; padding:10px; text-align:center; font-weight:bold; color:#065f46;">Microscopic structure</div>

</div>

<div style="text-align:center; margin-top:14px;">
  <div style="display:inline-block; background:linear-gradient(to right,#d1fae5,#cffafe,#dbeafe,#ede9fe,#fce7f3); border:1px solid rgba(107,114,128,0.16); padding:9px 18px; border-radius:7px; box-shadow:0 3px 10px rgba(15,23,42,0.08); font-size:0.76em; color:#374151; font-weight:bold;">A multiscale structure-to-property dependency</div>
</div>

---

## Method Landscape around a Central Theme

<div style="position:relative; margin-top:28px;">

<div style="display:grid; grid-template-columns:1fr 1fr; gap:18px;">

<div style="background:linear-gradient(135deg,#ecfeff,#cffafe); border:3px solid #06b6d4; border-radius:10px; padding:18px 16px; text-align:center; min-height:116px; display:flex; align-items:center; justify-content:center; color:#0e7490; font-weight:bold;">Method family A</div>
<div style="background:linear-gradient(135deg,#eff6ff,#bfdbfe); border:3px solid #3b82f6; border-radius:10px; padding:18px 16px; text-align:center; min-height:116px; display:flex; align-items:center; justify-content:center; color:#1e40af; font-weight:bold;">Method family B</div>
<div style="background:linear-gradient(135deg,#f5f3ff,#ddd6fe); border:3px solid #8b5cf6; border-radius:10px; padding:18px 16px; text-align:center; min-height:116px; display:flex; align-items:center; justify-content:center; color:#5b21b6; font-weight:bold;">Method family C</div>
<div style="background:linear-gradient(135deg,#ecfdf5,#a7f3d0); border:3px solid #10b981; border-radius:10px; padding:18px 16px; text-align:center; min-height:116px; display:flex; align-items:center; justify-content:center; color:#065f46; font-weight:bold;">Method family D</div>

</div>

<div style="position:absolute; top:50%; left:50%; transform:translate(-50%,-50%); background:rgba(255,255,255,0.38); -webkit-backdrop-filter:blur(10px) saturate(145%); backdrop-filter:blur(10px) saturate(145%); color:#1f2937; padding:14px 24px; border-radius:10px; font-weight:bold; font-size:0.78em; border:1.5px solid rgba(255,255,255,0.78); text-align:center; z-index:10; box-shadow:0 8px 24px rgba(15,23,42,0.18),inset 0 1px 0 rgba(255,255,255,0.72);">Central<br>Theme</div>

</div>

---

## Methods to Outputs

<div style="display:grid; grid-template-columns:1fr 64px 1fr; gap:0; margin-top:30px; align-items:center;">

<div style="display:flex; flex-direction:column; gap:10px;">

<div style="background:linear-gradient(135deg,#ecfeff,#a5f3fc); border:2px solid #06b6d4; border-radius:8px; padding:12px; text-align:center; font-weight:bold; color:#164e63;">Method A</div>
<div style="background:linear-gradient(135deg,#eff6ff,#bfdbfe); border:2px solid #3b82f6; border-radius:8px; padding:12px; text-align:center; font-weight:bold; color:#1e40af;">Method B</div>
<div style="background:linear-gradient(135deg,#f5f3ff,#ddd6fe); border:2px solid #8b5cf6; border-radius:8px; padding:12px; text-align:center; font-weight:bold; color:#5b21b6;">Method C</div>

</div>

<div style="text-align:center; font-size:1.8em; font-weight:bold; background:linear-gradient(90deg,#8b5cf6,#ec4899); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;">→</div>

<div style="display:flex; flex-direction:column; gap:8px;">

<div style="background:linear-gradient(135deg,#fdf2f8,#fce7f3); border:2px solid #ec4899; border-radius:8px; padding:9px; text-align:center; color:#9f1239; font-weight:bold;">Output A</div>
<div style="background:linear-gradient(135deg,#fff1f2,#ffe4e6); border:2px solid #d93a49; border-radius:8px; padding:9px; text-align:center; color:#7f0000; font-weight:bold;">Output B</div>
<div style="background:linear-gradient(135deg,#fff7ed,#fef3c7); border:2px solid #f59e0b; border-radius:8px; padding:9px; text-align:center; color:#92400e; font-weight:bold;">Output C</div>
<div style="background:linear-gradient(135deg,#fefce8,#fef9c3); border:2px solid #eab308; border-radius:8px; padding:9px; text-align:center; color:#854d0e; font-weight:bold;">Output D</div>

</div>

</div>

<div style="text-align:center; margin-top:14px; color:#64748b; font-size:0.72em;">Methods on the left map to interpretable quantities or capabilities on the right.</div>

---

<center>

# Thank You!

## Comments and suggestions are welcome

</center>
