# Awesome 3DGS Papers

A curated, review-oriented index of core and representative papers on **3D Gaussian Splatting (3DGS)**, with paper links, official code links where available, concise contribution notes, and a machine-readable CSV.

面向综述写作的 3DGS 论文索引：按研究主题整理核心与代表性工作，并记录论文、代码、贡献摘要和链接核验日期。

> This is a curated starting point, not an exhaustive bibliography. Categories and priorities reflect the current review taxonomy and may overlap.

## Taxonomy

| Category | Papers |
| --- | ---: |
| Foundations & optimization | 3 |
| Surveys & benchmarks | 4 |
| Dynamic / 4D | 6 |
| Generation | 2 |
| Rasterization & anti-aliasing | 3 |
| Compression & efficiency | 6 |
| Geometry & surface | 3 |
| Sparse-view & generalizable | 5 |
| SLAM & robotics | 6 |
| Semantics & editing | 4 |
| Large-scale & distributed | 5 |
| **Total** | **47** |

## Papers

### Foundations & optimization

- **3D Gaussian Splatting for Real-Time Radiance Field Rendering** (2023) — SIGGRAPH 2023 · arXiv:2308.04079 · Core. [Paper](https://arxiv.org/abs/2308.04079) · [Code](https://github.com/graphdeco-inria/gaussian-splatting). Introduces anisotropic 3D Gaussians, interleaved optimization and density control, and visibility-aware differentiable rasterization.
- **Scaffold-GS: Structured 3D Gaussians for View-Adaptive Rendering** (2023) — CVPR 2024 Highlight · arXiv:2312.00109 · Core. [Paper](https://arxiv.org/abs/2312.00109) · [Code](https://github.com/city-super/Scaffold-GS). Replaces unconstrained per-view Gaussian growth with structured anchors and view-adaptive local Gaussians.
- **3D Gaussian Splatting as Markov Chain Monte Carlo** (2024) — NeurIPS 2024 Spotlight · arXiv:2404.09591 · Core. [Paper](https://arxiv.org/abs/2404.09591) · [Code](https://github.com/ubc-vision/3dgs-mcmc). Reframes Gaussian density control as an MCMC process to reduce hand-designed densification heuristics.

### Surveys & benchmarks

- **A Survey on 3D Gaussian Splatting** (2024) — arXiv survey; revised 2026 · arXiv:2401.03890 · Survey. [Paper](https://arxiv.org/abs/2401.03890). A broad, frequently revised field overview; use its taxonomy and references as a map into primary papers.
- **3D Gaussian Splatting: Survey, Technologies, Challenges, and Opportunities** (2024) — IEEE TCSVT 2025 · arXiv:2407.17418 · Survey. [Paper](https://arxiv.org/abs/2407.17418). Organizes optimization, technical modules, applications, challenges, and opportunities across 3DGS.
- **A Survey on 3D Gaussian Splatting Applications: Segmentation, Editing, and Generation** (2025) — arXiv survey; revised 2026 · arXiv:2508.09977 · Survey. [Paper](https://arxiv.org/abs/2508.09977). Recent application-focused review of segmentation, editing, generation, supervision, benchmarks, and evaluation.
- **Compression in 3D Gaussian Splatting: A Survey of Methods, Trends, and Future Directions** (2025) — arXiv survey · arXiv:2502.19457 · Survey. [Paper](https://arxiv.org/abs/2502.19457). Dedicated taxonomy and comparison of 3DGS compression methods and deployment trade-offs.

### Dynamic / 4D

- **Dynamic 3D Gaussians: Tracking by Persistent Dynamic View Synthesis** (2023) — CVPR 2024 · arXiv:2308.09713 · Core. [Paper](https://arxiv.org/abs/2308.09713) · [Code](https://github.com/JonathonLuiten/Dynamic3DGaussians). Early dynamic 3DGS work that jointly models view synthesis and dense 6-DoF tracking with persistent Gaussians.
- **Deformable 3D Gaussians for High-Fidelity Monocular Dynamic Scene Reconstruction** (2023) — CVPR 2024 · arXiv:2309.13101 · Core. [Paper](https://arxiv.org/abs/2309.13101) · [Code](https://github.com/ingra14m/Deformable-3D-Gaussians). Uses canonical Gaussians with a learned deformation field to reconstruct monocular dynamic scenes.
- **4D Gaussian Splatting for Real-Time Dynamic Scene Rendering** (2023) — CVPR 2024 · arXiv:2310.08528 · Core. [Paper](https://arxiv.org/abs/2310.08528) · [Code](https://github.com/hustvl/4DGaussians). Extends 3DGS to dynamic scenes with a time-conditioned deformation representation and real-time rendering.
- **4D Gaussian Splatting: Modeling Dynamic Scenes with Native 4D Primitives** (2024) — arXiv preprint; revised 2025 · arXiv:2412.20720 · Representative. [Paper](https://arxiv.org/abs/2412.20720). Models space-time jointly with native 4D Gaussian primitives instead of relying only on deformation of 3D Gaussians.
- **Hybrid 3D-4D Gaussian Splatting for Fast Dynamic Scene Representation** (2025) — arXiv preprint · arXiv:2505.13215 · Representative. [Paper](https://arxiv.org/abs/2505.13215). Keeps static regions in 3D Gaussians and assigns native 4D Gaussians to dynamic regions.
- **Disentangled 4D Gaussian Splatting: Rendering High-Resolution Dynamic World at 343 FPS** (2025) — arXiv preprint · arXiv:2503.22159 · Representative. [Paper](https://arxiv.org/abs/2503.22159). Separates spatial and temporal components to reduce redundant 4D computations.

### Generation

- **GaussianDreamer: Fast Generation from Text to 3D Gaussians by Bridging 2D and 3D Diffusion Models** (2023) — CVPR 2024 · arXiv:2310.08529 · Representative. [Paper](https://arxiv.org/abs/2310.08529) · [Code](https://github.com/hustvl/GaussianDreamer). Connects 2D and 3D diffusion priors for text-to-3D Gaussian asset generation.
- **DreamGaussian: Generative Gaussian Splatting for Efficient 3D Content Creation** (2023) — ICLR 2024 Oral · arXiv:2309.16653 · Representative. [Paper](https://arxiv.org/abs/2309.16653) · [Code](https://github.com/dreamgaussian/dreamgaussian). Uses Gaussian optimization and mesh extraction for efficient image- and text-conditioned 3D content creation.

### Rasterization & anti-aliasing

- **Mip-Splatting: Alias-free 3D Gaussian Splatting** (2023) — CVPR 2024 Best Student Paper · arXiv:2311.16493 · Core. [Paper](https://arxiv.org/abs/2311.16493) · [Code](https://github.com/autonomousvision/mip-splatting). Addresses scale changes and aliasing with 3D smoothing and a 2D Mip filter.
- **StopThePop: Sorted Gaussian Splatting for View-Consistent Real-time Rendering** (2024) — SIGGRAPH Asia 2024 · arXiv:2402.00525 · Core. [Paper](https://arxiv.org/abs/2402.00525) · [Code](https://github.com/r4dl/StopThePop). Improves depth ordering to reduce popping and blending artifacts as the camera moves.
- **SA-GS: Scale-Adaptive Gaussian Splatting for Training-Free Anti-Aliasing** (2024) — CVPR 2024 · arXiv:2403.19615 · Representative. [Paper](https://arxiv.org/abs/2403.19615). Adds test-time scale-adaptive filtering and pixel integration for anti-aliasing pretrained splats.

### Compression & efficiency

- **LightGaussian: Unbounded 3D Gaussian Compression with 15x Reduction and 200+ FPS** (2023) — NeurIPS 2024 Spotlight · arXiv:2311.17245 · Representative. [Paper](https://arxiv.org/abs/2311.17245) · [Code](https://github.com/VITA-Group/LightGaussian). Combines pruning, distillation, and vector quantization to reduce model size and speed rendering.
- **CompGS: Smaller and Faster Gaussian Splatting with Vector Quantization** (2023) — ECCV 2024 · arXiv:2311.18159 · Representative. [Paper](https://arxiv.org/abs/2311.18159) · [Code](https://github.com/chaffim/compact3d_DC3D). Compresses Gaussian parameters with vector quantization to reduce storage and improve rendering efficiency.
- **Mini-Splatting: Representing Scenes with a Constrained Number of Gaussians** (2024) — ECCV 2024 · arXiv:2403.14166 · Representative. [Paper](https://arxiv.org/abs/2403.14166) · [Code](https://github.com/fatPeter/mini-splatting). Studies compact scene representations under a constrained Gaussian budget.
- **HAC: Hash-grid Assisted Context for 3D Gaussian Splatting Compression** (2024) — ECCV 2024 · arXiv:2403.14530 · Core. [Paper](https://arxiv.org/abs/2403.14530) · [Code](https://github.com/YihangChen-ee/HAC). Uses spatial context and entropy coding to compress Gaussian attributes.
- **ContextGS: Compact 3D Gaussian Splatting with Anchor Level Context Model** (2024) — NeurIPS 2024 · arXiv:2405.20721 · Representative. [Paper](https://arxiv.org/abs/2405.20721) · [Code](https://github.com/wyf0912/ContextGS). Models anchor-level context to improve compact Gaussian representation and coding.
- **Taming 3DGS: High-Quality Radiance Fields with Limited Resources** (2024) — SIGGRAPH Asia 2024 · arXiv:2406.15643 · Representative. [Paper](https://arxiv.org/abs/2406.15643) · [Code](https://github.com/humansensinglab/taming-3dgs). Explores efficient 3DGS training and representation under constrained compute and memory.

### Geometry & surface

- **SuGaR: Surface-Aligned Gaussian Splatting for Efficient 3D Mesh Reconstruction and High-Quality Mesh Rendering** (2023) — CVPR 2024 · arXiv:2311.12775 · Core. [Paper](https://arxiv.org/abs/2311.12775) · [Code](https://github.com/Anttwo/SuGaR). Regularizes Gaussians toward surfaces and supports efficient mesh extraction and mesh-compatible rendering.
- **Gaussian Opacity Fields: Efficient Adaptive Surface Reconstruction in Unbounded Scenes** (2024) — SIGGRAPH Asia 2024 / TOG · arXiv:2404.10772 · Core. [Paper](https://arxiv.org/abs/2404.10772) · [Code](https://github.com/autonomousvision/gaussian-opacity-fields). Builds an opacity field over Gaussians for adaptive, efficient surface reconstruction in unbounded scenes.
- **2D Gaussian Splatting for Geometrically Accurate Radiance Fields** (2024) — SIGGRAPH 2024 · arXiv:2403.17888 · Core. [Paper](https://arxiv.org/abs/2403.17888) · [Code](https://github.com/hbb1/2d-gaussian-splatting). Uses oriented planar Gaussian disks and ray-splat intersections to improve geometric consistency and surface reconstruction.

### Sparse-view & generalizable

- **SparseGS: Sparse View Synthesis using 3D Gaussian Splatting** (2023) — 3DV 2025; revised 2026 · arXiv:2312.00206 · Representative. [Paper](https://arxiv.org/abs/2312.00206). Uses depth priors and unseen-view regularization to reduce floaters and collapse under sparse input views.
- **FSGS: Real-Time Few-shot View Synthesis using Gaussian Splatting** (2023) — ECCV 2024 · arXiv:2312.00451 · Representative. [Paper](https://arxiv.org/abs/2312.00451) · [Code](https://github.com/VITA-Group/FSGS). Targets few-shot novel-view synthesis and demonstrates reconstruction from very few training views.
- **pixelSplat: 3D Gaussian Splats from Image Pairs for Scalable Generalizable 3D Reconstruction** (2023) — CVPR 2024 Oral; Best Paper Runner-Up · arXiv:2312.12337 · Core. [Paper](https://arxiv.org/abs/2312.12337) · [Code](https://github.com/dcharatan/pixelsplat). Predicts a Gaussian scene feed-forward from image pairs for generalizable reconstruction.
- **MVSplat: Efficient 3D Gaussian Splatting from Sparse Multi-View Images** (2024) — ECCV 2024 Oral · arXiv:2403.14627 · Representative. [Paper](https://arxiv.org/abs/2403.14627) · [Code](https://github.com/donydchen/mvsplat). Uses plane-swept cost volumes to predict clean Gaussians feed-forward from sparse views.
- **GaussianPro: 3D Gaussian Splatting with Progressive Propagation** (2024) — ICML 2024 · arXiv:2402.14650 · Representative. [Paper](https://arxiv.org/abs/2402.14650) · [Code](https://github.com/kcheng1021/GaussianPro). Progressively propagates geometry to improve reconstruction where SfM initialization is sparse or weak.

### SLAM & robotics

- **GS-SLAM: Dense Visual SLAM with 3D Gaussian Splatting** (2023) — CVPR 2024 Highlight · arXiv:2311.11700 · Core. [Paper](https://arxiv.org/abs/2311.11700). Introduces a real-time splatting map representation into dense visual SLAM.
- **Photo-SLAM: Real-time Simultaneous Localization and Photorealistic Mapping for Monocular, Stereo, and RGB-D Cameras** (2023) — CVPR 2024 · arXiv:2311.16728 · Representative. [Paper](https://arxiv.org/abs/2311.16728) · [Code](https://github.com/HuajianUP/Photo-SLAM). Combines visual SLAM with photorealistic Gaussian mapping across common camera setups.
- **Gaussian Splatting SLAM** (2023) — CVPR 2024 Highlight; Best Demo Award · arXiv:2312.06741 · Core. [Paper](https://arxiv.org/abs/2312.06741) · [Code](https://github.com/muskie82/MonoGS). Adapts 3DGS to monocular SLAM and unifies tracking, mapping, and rendering in a Gaussian scene representation.
- **SplaTAM: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM** (2023) — CVPR 2024 · arXiv:2312.02126 · Core. [Paper](https://arxiv.org/abs/2312.02126) · [Code](https://github.com/spla-tam/SplaTAM). Uses explicit volumetric Gaussians for dense reconstruction from an unposed RGB-D stream.
- **Gaussian-SLAM: Photo-realistic Dense SLAM with Gaussian Splatting** (2023) — Research paper / arXiv · arXiv:2312.10070 · Representative. [Paper](https://arxiv.org/abs/2312.10070) · [Code](https://github.com/VladimirYugay/Gaussian-SLAM). Explores dense photorealistic SLAM with 3DGS as the scene representation.
- **RTG-SLAM: Real-time 3D Reconstruction at Scale using Gaussian Splatting** (2024) — SIGGRAPH 2024 · arXiv:2404.19706 · Representative. [Paper](https://arxiv.org/abs/2404.19706) · [Code](https://github.com/MisEty/RTG-SLAM). Targets real-time reconstruction at scale using a Gaussian SLAM pipeline.

### Semantics & editing

- **Gaussian Grouping: Segment and Edit Anything in 3D Scenes** (2023) — ECCV 2024 · arXiv:2312.00732 · Core. [Paper](https://arxiv.org/abs/2312.00732) · [Code](https://github.com/lkeab/gaussian-grouping). Lifts 2D segmentation cues into 3D Gaussians for open-world object grouping and scene editing.
- **Feature 3DGS: Supercharging 3D Gaussian Splatting to Enable Distilled Feature Fields** (2023) — CVPR 2024 Highlight · arXiv:2312.03203 · Representative. [Paper](https://arxiv.org/abs/2312.03203) · [Code](https://github.com/ShijieZhou-UCLA/feature-3dgs). Distills 2D foundation-model features into Gaussians for open-vocabulary 3D feature fields.
- **LangSplat: 3D Language Gaussian Splatting** (2023) — CVPR 2024 Highlight · arXiv:2312.16084 · Representative. [Paper](https://arxiv.org/abs/2312.16084) · [Code](https://github.com/minghanqin/LangSplat). Encodes language-aligned features in Gaussians for open-vocabulary spatial queries.
- **GaussianEditor: Swift and Controllable 3D Editing with Gaussian Splatting** (2023) — CVPR 2024 · arXiv:2311.14521 · Representative. [Paper](https://arxiv.org/abs/2311.14521) · [Code](https://github.com/buaacyw/GaussianEditor). Provides controllable editing operations on Gaussian scenes while preserving multi-view consistency.

### Large-scale & distributed

- **CityGaussian: Real-time High-quality Large-Scale Scene Rendering with Gaussians** (2024) — ECCV 2024 · arXiv:2404.01133 · Core. [Paper](https://arxiv.org/abs/2404.01133) · [Code](https://github.com/Linketic/CityGaussian). Uses divide-and-conquer scene partitioning and level of detail for city-scale reconstruction and rendering.
- **VastGaussian: Vast 3D Gaussians for Large Scene Reconstruction** (2024) — CVPR 2024 · arXiv:2402.17427 · Representative. [Paper](https://arxiv.org/abs/2402.17427). Partitions large scenes for parallel optimization and models appearance variation at scale.
- **Octree-GS: Towards Consistent Real-time Rendering with LOD-Structured 3D Gaussians** (2024) — TPAMI 2025 · arXiv:2403.17898 · Representative. [Paper](https://arxiv.org/abs/2403.17898) · [Code](https://github.com/city-super/Octree-GS). Uses octree and level-of-detail structure for consistent real-time rendering across scene scales.
- **On Scaling Up 3D Gaussian Splatting Training** (2024) — ICLR 2025 Oral · arXiv:2406.18533 · Representative. [Paper](https://arxiv.org/abs/2406.18533). Presents Grendel, a distributed multi-GPU system for scaling 3DGS training to large scenes.
- **Immediate 3D Gaussian Splat Reconstruction of Unordered Input with Global Consistency** (2026) — SIGGRAPH 2026 · arXiv:2607.14481 · Representative. [Paper](https://arxiv.org/abs/2607.14481) · [Code](https://github.com/graphdeco-inria/i3dgs). Combines immediate feedback, unordered image matching, loop closure, and progressive hierarchy for large captures.

## Data file

[`papers.csv`](papers.csv) contains the same records with stable paper IDs, categories, publication status, paper and code URLs, code status, review priority, cross-cutting tags, input/output summary, and link-check date.

## Curation and maintenance

- Include work that introduces or materially advances 3DGS methods, surveys or benchmarks the field, or provides a representative application.
- Keep titles and arXiv identifiers aligned with the linked paper. Prefer the authors' project page or repository for code links.
- Mark code as unavailable when no official implementation can be confirmed; do not replace it with an unverified third-party port.
- Use multiple categories when a paper materially spans review branches. The categories are for navigation, not mutually exclusive scientific claims.
- Check links when adding or editing records, and update the `Link checked on` field in the CSV.
- Contributions and corrections are welcome through pull requests.

## Related indexes

This paper-focused index complements broader 3DGS resource collections:
- [MrNeRF/awesome-3D-gaussian-splatting](https://github.com/MrNeRF/awesome-3D-gaussian-splatting)
- [AIG3DX/Awesome-3DGS](https://github.com/AIG3DX/Awesome-3DGS)

## Link status

The source research table marked paper links and listed official code repositories as checked on **2026-11-03**. Link availability and publication status can change; please report corrections.
