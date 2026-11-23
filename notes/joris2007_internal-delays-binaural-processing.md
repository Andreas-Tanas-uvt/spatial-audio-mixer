# A matter of time: internal delays in binaural processing

* **Source PDF:** `../papers/1-s2.0-S016622360600275X-main.pdf`
* **BibTeX Key:** `joris2007matter`
* **Bibliographic Info:** P. Joris & T. C. T. Yin, *"A matter of time: internal delays in binaural processing,"* *Trends in Neurosciences*, Vol. 30, No. 2, pp. 70–78, 2007.

## Core Contribution
Reviews the neurophysiological mechanisms behind Interaural Time Difference (ITD) sensitivity, frequency-dependent Best Delay (BD) distributions, and interaural correlation ($\rho$) processing in the mammalian auditory brainstem and midbrain.

## Relevant Information
* Humans have an ecological ITD range of roughly $\pm 700\,\mu\text{s}$ and can discriminate ITD changes as small as $10\text{--}20\,\mu\text{s}$.
* Low-frequency ongoing ITDs dominate horizontal localization, while above $\sim 1.5\text{ kHz}$ fine-structure phase becomes ambiguous and envelope/level cues take over.
* Binaural sensitivity is governed not only by static ITDs, but also by **interaural correlation ($\rho$)**—decorrelation produces perceived "spaciousness" and aids signal detection in complex multi-source environments (human $\Delta\rho$ thresholds $\approx 0.006$).

## Role in Thesis (Real-Time IEM Spatial Mixer)
* Sets precision targets for sub-millisecond ITD delay lines (requiring fractional-delay interpolation with $<10\,\mu\text{s}$ accuracy).
* Justifies separating low-frequency ITD fine-structure processing from high-frequency ILD/envelope processing at the $\sim 1.5\text{ kHz}$ crossover.
* Informs decorrelation/reverb bus design so dense stage mixes achieve externalized "spaciousness" without degrading pitch or onset clarity.
