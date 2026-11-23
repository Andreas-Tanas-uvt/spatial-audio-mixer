# Binaural Hearing (MIT HST.723 Lecture Notes)

* **Source PDF:** `../papers/a97104b00fd0c985c770ed1eb2bd2b02_t3_binaural.pdf`
* **BibTeX Key:** `oxenham2005binaural`
* **Bibliographic Info:** A. J. Oxenham, *"Binaural Hearing,"* Lecture Notes for HST.723: Neural Coding and Perception of Sound, Harvard-MIT Division of Health Sciences and Technology, 2005.

## Core Contribution
Concise psychoacoustic reference covering Duplex Theory, Minimum Audible Angles (MAA), the Cone of Confusion, the Precedence Effect (Haas effect), Binaural Masking Level Differences (BMLD), and binaural sluggishness.

## Relevant Information
* **Quantitative JND Benchmarks:** $1^\circ$ azimuth $\approx 10\,\mu\text{s}$ ITD; lowest JNDs are $10\,\mu\text{s}$ ITD and $0.5\text{--}1\text{ dB}$ ILD; localization degrades around $1.5\text{--}3\text{ kHz}$ (Duplex Theory crossover).
* **Precedence Effect Time Windows:** $<1\text{ ms}$ produces summing localization; $1\text{--}5\text{ ms}$ fuses reflections to the first-arriving wavefront; $>5\text{ ms}$ exceeds echo threshold for clicks.
* **Binaural Sluggishness:** The auditory system cannot track spatial motion faster than $\sim 3\text{ Hz}$ (above $10\text{--}20\text{ Hz}$ motion blurs completely).
* **BMLD:** Up to $15\text{ dB}$ unmasking in broadband noise via interaural phase/spatial separation.

## Role in Thesis (Real-Time IEM Spatial Mixer)
* Establishes hard perceptual constraints for the engine: early reflections in virtual room models must stay within the $1\text{--}5\text{ ms}$ precedence window to avoid discrete echoes, while head-tracker/panning smoothing filters only need to preserve updates up to $\sim 3\text{--}10\text{ Hz}$ without audible stepping.
