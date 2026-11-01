# Audio-Visual Spatial Correspondence Learning

## Research question
Can semantic and spatial audio-visual correspondence objectives learn complementary representations useful for visually guided mono-to-binaural audio generation?

## Approach
- Visual features from frozen DINOv2 (with registers) and DINOv3 vision transformers.
- Semantic correspondence between video/image features and mono audio.
- Spatial correspondence between video/image features and binaural spatial cues, including interaural differences.
- Contrastive learning alongside a visually conditioned reconstruction objective.
- Comparisons of dense token similarity aggregation, shared projections, and decoder conditioning.

## Selected experimental evidence
For the recorded 104-clip **seen-category** ablation using the same evaluation setup:

| Configuration | STFT distance ↓ | Envelope distance ↓ |
| --- | ---: | ---: |
| Multi-head, product → pool | **0.817257** | **0.128432** |
| Multi-head, pool → product | 0.830878 | 0.129352 |
| Mono-only single-head, pool → product | 0.831159 | 0.129419 |
| Mono-only single-head, product → pool | 0.832363 | 0.130012 |

These are reconstruction metrics, not direct proof of semantic/spatial disentanglement. The single-head comparisons also change more than just head count, so they do not isolate that factor.

## Limitations and lessons
- A historically labeled `unseen1` split was subsequently identified as **seen-category**; claims were corrected accordingly.
- A true category-unseen follow-up showed a generalization gap for held-out categories, rather than establishing generalization.
- Diagnostic retrieval and visualizations suggest complementary behavior but do not independently prove complete separation of semantics and spatial information.
- Some later analyses are recorded in research notes rather than fully reproducible public code.

## Status
Research summary only. Implementation and datasets are not published through this portfolio. Code release depends on provenance, licensing, and any required collaborator approval.
