# Wafer Defect Classification

## Problem
Classify visual wafer-die images across five categories: DIE_BROKEN, DIE_CRACK, DIE_INK, NORMAL, and NO_DIE, while evaluating performance on a target acquisition domain.

## Experiments
- Baseline: ResNet-18 trained on target-domain (G4) images.
- Domain-data comparison: G4-only training versus G4+G5 training, with G4 validation.
- Backbone exploration: ResNet-18, ResNet-152, and EfficientNet-B0.
- Augmentation: brightness and contrast perturbations using color jitter.

## Recorded results
- In one initial ResNet-18 comparison, validation F1 improved from approximately **0.55** (G4-only training) to **0.75** (G4+G5 training).
- Later backbone experiments recorded F1 of approximately **0.8493** (EfficientNet-B0), **0.8284** (ResNet-18), and **0.8738** (ResNet-152) in their respective summarized comparisons.
- The best recorded individual ResNet-152 configuration reached approximately **0.8942** F1.

These figures come from different experimental comparisons and should not be treated as controlled head-to-head results without matching splits and settings.

## Lessons and limitations
Additional training-domain coverage improved this target validation setting, while larger backbones increased computational cost. Results are dataset-specific and do not establish out-of-domain robustness without further evaluation.

## Status
Summary only. Proprietary or otherwise non-cleared dataset images, weights, and training files are not included.
