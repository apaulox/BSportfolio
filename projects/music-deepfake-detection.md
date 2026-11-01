# Music Deepfake Detection

## Problem
Distinguish authentic audio from generated or manipulated content, considering both **vocal** and **musical** characteristics.

## Approach
- Explored pretrained audio encoders for speech and music.
- Compared input processing with and without source separation via HTDemucs.
- Investigated classifier fusion, augmentation, evaluation, and self-contained inference packaging.
- Organized experiment logs and evaluation checks to support comparisons.

## Research considerations
Different components may respond differently to vocal synthesis, instrument generation, compression, and distribution shifts. A system-level performance change should be evaluated alongside component-level metrics and the input/preprocessing conditions.

## Status and limitations
This is an ongoing project summary rather than a claim of benchmark-leading performance. Training data, model artifacts, submission packages, and private implementation remain outside this public repository. Any future release should verify dataset and pretrained-model licensing requirements.
