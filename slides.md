---
title-slide: false
bibliography: references.bib
csl: vancouver.csl
citeproc: true
theme: serif
background-color: "#ffffff"
transition: slide
navigationMode: linear
hash: true
---

:::: {.columns}
::: {.column width="50%"}

## Sample slides
#### PlaceHolderName
#### Universiti Malaysia Perlis
#### [placeholder@email.com](mailto:placeholder@email.com)

<audio id="bg-music" src="media/audio/sb.m4a" loop></audio>

<div id="audio-credit"
     style="position: absolute; bottom: 40px; right: 20px; font-size: 0.6em; opacity: 0.6;">
  Music: “Adrift” by Scott Buckley (CC BY 4.0)
</div>

<script>
  document.addEventListener('DOMContentLoaded', () => {
    const audio = document.getElementById('bg-music');
    const credit = document.getElementById('audio-credit');

    // hide credit by default
    credit.style.display = 'none';

    const test = new Audio('media/audio/bgm.mp3');

    test.addEventListener('canplaythrough', () => {
      // bgm.mp3 exists → use it, keep credit hidden
      audio.src = 'media/audio/bgm.mp3';
    }, { once: true });

    test.addEventListener('error', () => {
      // bgm.mp3 missing → sb.m4a will play → show credit
      credit.style.display = 'block';
    }, { once: true });

    document.addEventListener('click', () => {
      if (Reveal.getIndices().h === 0) {
        audio.volume = 0.5;
        audio.play();
      }
    }, { once: true });

    Reveal.on('slidechanged', (event) => {
      if (event.indexh > 0) { audio.pause(); }
      else { audio.play(); }
    });
  });
</script>

:::

::: {.column width="50%"}
![](media/pics/logo1.png)
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Slide one
**Key Concepts:**
- Energy conservation per @carnot1824.
- $\Delta U = Q - W$
:::

::: {.column width="50%"}
![](media/pics/sample.png)
:::
::::

---

<span class="slide-title" data-title="My Hidden Slide Name"></span>

![](media/pics/wide.jpeg)

---

:::: {.columns}
::: {.column width="50%"}
### The Master Equation
The fundamental relation of thermodynamics:

$$\Delta U = Q - W$$

The work done $W$ is positive when the system expands against an external pressure.
:::

::: {.column width="50%"}
<video data-src="media/videos/sample.mp4" data-autoplay loop muted width="100%"></video>
:::

::::

---

:::: {.columns}
::: {.column width="50%"}
### Visualizing the Gas Law
**Interactive Model:**

- P, V, and T relationships.
- Use the slider to adjust pressure.
- Observe the phase boundary.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/sample.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

---

# Bibliography
<div id="refs"></div>

---

:::: {.columns}
::: {.column width="50%"}
### Math Scores by Gender

This boxplot illustrates the distribution of Math scores across different genders in the `bigclass` dataset.

**Observations:**
- Provides a visual summary of central tendency and variability.
- Helps identify potential differences or outliers in scores between groups.
:::

::: {.column width="50%"}
<iframe 
  data-src="media/plots/math_vs_gender_boxplot.html" 
  width="100%" 
  height="500px" 
  style="border:none;" 
  scrolling="no">
</iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Control Chart: Machine 1
**Conditions:** 200kPa, 338K.

This X-bar chart monitors the stability of the production process for Machine 1.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/xbar_m1_200_338.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Control Chart: Machine 2
**Conditions:** 200kPa, 338K.

This chart highlights the variation in PartLength for Machine 2.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/xbar_m2_200_338.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Control Chart: Machine 3
**Conditions:** 200kPa, 338K.

Statistical control limits for Machine 3 under standard operating conditions.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/xbar_m3_200_338.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Process Capability: Machine 1
**Conditions:** 200kPa, 338K

**Specifications:**
- LSL: 45mm
- USL: 55mm
- Target: 50mm

**Analysis:**
- The histogram shows the distribution of produced parts against limits.
- $C_{pk}$ measures how centered the process is relative to specs.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/cpk_m1_200_338.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Revised Process Capability
**Machine 1: Overall Performance**

By analyzing all data points for Machine 1, we obtain a realistic view of the process spread:

- **Distribution:** The histogram now reflects the actual variance in production.
- **Performance:** This chart provides the valid $C_{pk}$ and $C_p$ indices used for quality assessment.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/cpk_m1_full.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 1 Process Capability
**Final Corrected Analysis**

Using the full variation found in the Machine 1 dataset:

- **Targeting:** Assessing performance against the 50mm target.
- **Spread:** The actual standard deviation is used to calculate realistic indices.
- **Quality:** High $C_{pk}$ suggests the process is well within limits.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/cpk_m1_corrected.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Machine 1 Analysis (200kPa)
**Process Control Chart**

This chart monitors the stability of Machine 1 when operating at a pressure of 200kPa.

- **Stability:** Checks for points exceeding the 3-sigma control limits.
- **Trend:** Identifies systematic shifts in production length.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/xbar_m1_200.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="50%"}
### Process Capability (200kPa)
**Machine 1 Performance**

This distribution plot shows the process capability specifically at 200kPa pressure.

- **Targeting:** Centers around the 50mm requirement.
- **Precision:** Evaluates how much of the production falls within the 45-55mm limits.
- **Metric:** The $C_{pk}$ index quantifies the process potential.
:::

::: {.column width="50%"}
<iframe data-src="media/plots/cpk_m1_200.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="40%"}
### Process Capability (200kPa)
**Machine 1 Performance**

Statistical analysis of production quality at operating pressure = 200kPa.

- **Metric:** $C_{pk}$ index quantifies centering and spread.
- **Precision:** The distribution relative to [45, 55] limits.
- **Stability:** Evaluated through natural process variation.
:::

::: {.column width="60%"}
<iframe data-src="media/plots/cpk_m1_200.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="40%"}
### Process Capability
**Machine 1 @ 200kPa**

Statistical distribution and centering for Machine 1 under 200kPa pressure.

- **Target:** 50mm
- **Limits:** [45, 55]
- **Result:** High $C_{pk}$ indicates the process is stable and well within specifications.
:::

::: {.column width="60%"}
<iframe data-src="media/plots/cpk_m1_200.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="40%"}
### Process Capability (n=200)
**Machine 1 @ 200kPa**

Analysis focused on a specific sample size of 200 observations.

- **Sample Size:** 200 units
- **Metrics:** Centering and spread indices updated for the subset.
- **Status:** Evaluation of process potential relative to [45, 55] limits.
:::

::: {.column width="60%"}
<iframe data-src="media/plots/cpk_m1_200_forced.html" width="100%" height="500px" style="border:none;"></iframe>
:::
::::

---

:::: {.columns}
::: {.column width="40%"}
### Process Capability (n=200)
**Machine 2 @ 200kPa**

Comparison analysis for Machine 2 under identical 200kPa conditions.

- **Sample Size:** 200 units
- **Metric:** Centering and spread for Machine 2.
- **Performance:** Assessing if Machine 2 meets [45, 55] limits as effectively as Machine 1.
:::

::: {.column width="60%"}
<iframe data-src="media/plots/cpk_m2_200_forced.html" width="100%" height="500px" style="border:none;"></iframe>
::: 
::::

---

:::: {.columns}
::: {.column width="40%"}
### Process Capability (n=200)
**Machine 3 @ 200kPa**

Comparison analysis for Machine 3 under identical 200kPa conditions.

- **Sample Size:** 200 units
- **Metric:** Centering and spread for Machine 3.
- **Performance:** Assessing if Machine 3 meets [45, 55] limits as effectively as Machines 1 and 2.
:::

::: {.column width="60%"}
<iframe data-src="media/plots/cpk_m3_200_forced.html" width="100%" height="500px" style="border:none;"></iframe>
::: 
::::

---

:::: {.columns}
::: {.column width="40%"}
### Control Chart: Machine 1
**200kPa @ 338K**

Process stability check for Machine 1.

- **Type:** X-bar (Individuals)
- **Parameters:** P=200, T=338
- **Status:** Reviewing for points beyond control limits (UCL/LCL).
:::

::: {.column width="60%"}
<iframe data-src="media/plots/xbar_m1_200_338.html" width="100%" height="500px" style="border:none;"></iframe>
::: 
::::

---

:::: {.columns}
::: {.column width="40%"}
### Control Chart: Machine 2
**200kPa @ 338K**

Process stability check for Machine 2.

- **Type:** X-bar (Individuals)
- **Parameters:** P=200, T=338
- **Status:** Comparison against Machine 1 performance.
:::

::: {.column width="60%"}
<iframe data-src="media/plots/xbar_m2_200_338.html" width="100%" height="500px" style="border:none;"></iframe>
::: 
::::

---

:::: {.columns}
::: {.column width="40%"}
### Control Chart: Machine 3
**200kPa @ 338K**

Process stability check for Machine 3.

- **Type:** X-bar (Individuals)
- **Parameters:** P=200, T=338
- **Status:** Evaluating consistency across the production line.
:::

::: {.column width="60%"}
<iframe data-src="media/plots/xbar_m3_200_338.html" width="100%" height="500px" style="border:none;"></iframe>
::: 
::::

---

### Stability Overview: All Machines
**Comparison at 200kPa / 338K**

| Machine | Status | Observations |
| :--- | :--- | :--- |
| Machine 1 | Fixed Limits | 200 |
| Machine 2 | Fixed Limits | 200 |
| Machine 3 | Validated | 200 |

<iframe data-src="media/plots/xbar_fixed_m1.html" width="100%" height="400px" style="border:none;"></iframe>
<iframe data-src="media/plots/xbar_fixed_m2.html" width="100%" height="400px" style="border:none;"></iframe>
<iframe data-src="media/plots/xbar_fixed_m3.html" width="100%" height="400px" style="border:none;"></iframe>
