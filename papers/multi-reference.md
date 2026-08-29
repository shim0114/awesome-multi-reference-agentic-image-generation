# Multi-Reference Image Generation

[← Main list](../README.md) · [Agentic generation](agentic.md) ·
[Direct intersection](intersection.md) · [Contributing](../CONTRIBUTING.md)

> A curated bibliography of image-generation methods that consume **multiple visual references**: multiple subjects or identities, multiple personalized concepts, content–style/reference composition, and interleaved multimodal context.

**Last verified:** 2026-08-29  
**Coverage:** in-scope methods, dedicated benchmarks/datasets, and clearly
separated background foundations.

## Contents

- [Scope and verification policy](#scope-and-verification-policy)
- [Native multi-reference and interleaved context](#1-native-multi-reference-and-interleaved-context-generation)
- [Multi-subject and multi-identity personalization](#2-multi-subject-and-multi-identity-personalization)
- [Multi-concept and content–style composition](#3-multi-concept-and-contentstyle-composition)
- [Multiple-image aggregation](#4-multiple-image-aggregation-for-one-identity-or-concept)
- [Benchmarks and datasets](#5-dedicated-benchmarks-and-datasets)
- [Background foundations](#6-background-foundations--not-counted-as-direct-multi-reference-papers)

## Scope and verification policy

- Included: generation conditioned on two or more reference images, multi-subject/multi-identity personalization, multi-concept composition, content–style fusion, or a general model explicitly evaluated on multi-reference generation.
- Excluded: generic multi-view reconstruction, video-only identity consistency, ordinary single-reference editing, and methods that merely place text-specified objects without visual references.
- Sources are primary: official proceedings, arXiv/OpenReview paper records, author project pages, and author/organization repositories.
- A conference marked **author-reported** has not been independently verified in that venue's official proceedings as of the cutoff date.
- arXiv identifiers are shown explicitly. When an official proceedings title differs from the arXiv title, the proceedings title is used and the alias is noted.

### Artifact legend

- ✅ Official implementation and/or released model/data is available.
- 🧩 An official project page or repository exists, but the implementation is partial, promised, or not yet released.
- — No official artifact was located at the verification date.

## 1. Native multi-reference and interleaved-context generation

These models are designed around arbitrary or heterogeneous visual references rather than only merging separately trained personalization modules.

### 2026

- **MultiCompose: Multi-Concept Personalized Composition with Per-Subject Attribute Binding** — *arXiv preprint, 2026* · [paper: arXiv:2608.03708](https://arxiv.org/abs/2608.03708) · [code](https://github.com/I2-Multimedia-Lab/MultiCompose) ✅ — Binds attributes to the correct referenced subject and introduces MSP-Bench for dense multi-subject compositions.
- **StructGen: Disambiguating Multi-Reference Image Generation via Structured Context Modeling** — *arXiv preprint, 2026; ACM MM 2026 author-reported in the official repository* · [paper: arXiv:2607.15619](https://arxiv.org/abs/2607.15619) · [project](https://jianingpeng0382.github.io/StructGen/) · [repository](https://github.com/jianingPeng0382/StructGen) 🧩 — Converts ambiguous reference collections into structured subject/attribute relations before synthesis; the repository currently contains the project site rather than released training code.
- **Scaling Multi-Reference Image Generation with Dynamic Reward Optimization** — *arXiv preprint, 2026; ECCV 2026 Oral author-reported in the official repository* · [paper: arXiv:2606.26947](https://arxiv.org/abs/2606.26947) · [code](https://github.com/Weistrass/DyRef) ✅ — DyRef scales multi-reference generation with dynamic reward optimization and evaluates subject, attribute, and relation fidelity on OmniRef-Bench.
- **UniCustom: Unified Visual Conditioning for Multi-Reference Image Generation** — *arXiv preprint, 2026* · [paper: arXiv:2605.12088](https://arxiv.org/abs/2605.12088) · — — Uses one unified conditioning mechanism for heterogeneous combinations of subject, identity, style, and spatial references.
- **Multimodal Large Language Models for Multi-Subject In-Context Image Generation** — *ACL 2026 Long Paper* · [paper: ACL Anthology 2026.acl-long.1518](https://aclanthology.org/2026.acl-long.1518/) · [paper: arXiv:2604.07422](https://arxiv.org/abs/2604.07422) · — — MUSIC uses multimodal in-context reasoning and visual chain-of-thought layout planning for multi-subject generation.
- **MACRO: Advancing Multi-Reference Image Generation with Structured Long-Context Data** — *arXiv preprint, 2026* · [paper: arXiv:2603.25319](https://arxiv.org/abs/2603.25319) · [code and data](https://github.com/HKU-MMLab/Macro) ✅ — Trains on structured long-context data, supports as many as ten references, and contributes MacroData and MacroBench.
- **UniRef-Image-Edit: Towards Scalable and Consistent Multi-Reference Image Editing** — *arXiv preprint, 2026* · [paper: arXiv:2602.14186](https://arxiv.org/abs/2602.14186) · — — Unifies edit instructions and multi-image composition with self-generated supervision and multi-stage group-relative policy optimization; release is promised in the paper but was not located.
- **SIGMA: Selective-Interleaved Generation with Multi-Attribute Tokens** — *CVPR 2026* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2026/html/Zhang_SIGMA_Selective-Interleaved_Generation_with_Multi-Attribute_Tokens_CVPR_2026_paper.html) · [paper: arXiv:2602.07564](https://arxiv.org/abs/2602.07564) · [announced repository](https://github.com/auihund/SIGMA) 🧩 — Selectively composes heterogeneous subject, identity, content, and style attributes from interleaved references; CVF announces this code URL, but it returned 404 at verification time.

### 2025

- **LAMIC: Layout-Aware Multi-Image Composition via Scalability of Multimodal Diffusion Transformer** — *arXiv preprint, 2025* · [paper: arXiv:2508.00477](https://arxiv.org/abs/2508.00477) · [code](https://github.com/Suchenl/LAMIC) ✅ — Extends a multimodal diffusion transformer to many references without training and uses explicit layouts to reduce subject mixing.
- **OmniGen2: Exploration to Advanced Multimodal Generation** — *arXiv technical report, 2025* · [paper: arXiv:2506.18871](https://arxiv.org/abs/2506.18871) · [project](https://vectorspacelab.github.io/OmniGen2/) · [code](https://github.com/VectorSpaceLab/OmniGen2) ✅ — A unified generation/editing model whose in-context interface accepts multiple images and text for compositional synthesis.
- **Less-to-More Generalization: Unlocking More Controllability by In-Context Generation** — *ICCV 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/ICCV2025/html/Wu_Less-to-More_Generalization_Unlocking_More_Controllability_by_In-Context_Generation_ICCV_2025_paper.html) · [paper: arXiv:2504.02160](https://arxiv.org/abs/2504.02160) · [project](https://bytedance.github.io/UNO/) · [code](https://github.com/bytedance/UNO) ✅ — UNO learns unified in-context generation and generalizes from fewer conditions during training to multiple visual conditions at inference.
- **OmniGen: Unified Image Generation** — *CVPR 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2025/html/Xiao_OmniGen_Unified_Image_Generation_CVPR_2025_paper.html) · [paper: arXiv:2409.11340](https://arxiv.org/abs/2409.11340) · [code](https://github.com/VectorSpaceLab/OmniGen) ✅ — Treats text and one or more images as a single instruction sequence, enabling reference composition without task-specific adapters.

### 2024

- **UNIMO-G: Unified Image Generation through Multimodal Conditional Diffusion** — *ACL 2024 Long Paper* · [paper: ACL Anthology 2024.acl-long.335](https://aclanthology.org/2024.acl-long.335/) · [paper: arXiv:2401.13388](https://arxiv.org/abs/2401.13388) · — — Conditions diffusion on interleaved text and multiple image entities for subject-driven and compositional generation.
- **Instruct-Imagen: Image Generation with Multi-modal Instruction** — *CVPR 2024* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2024/html/Hu_Instruct-Imagen_Image_Generation_with_Multi-modal_Instruction_CVPR_2024_paper.html) · [paper: arXiv:2401.01952](https://arxiv.org/abs/2401.01952) · [project](https://instruct-imagen.github.io/) 🧩 — Learns heterogeneous multimodal instructions and includes tasks that combine multiple exemplar, subject, style, or control images.
- **Generative Multimodal Models are In-Context Learners** — *CVPR 2024* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2024/html/Sun_Generative_Multimodal_Models_are_In-Context_Learners_CVPR_2024_paper.html) · [paper: arXiv:2312.13286](https://arxiv.org/abs/2312.13286) · [code](https://github.com/baaivision/Emu) ✅ — Emu2 generates from interleaved multimodal contexts and demonstrates multi-reference subject/style composition through in-context learning.
- **Context Diffusion: In-Context Aware Image Generation** — *ECCV 2024* · [paper: arXiv:2312.03584](https://arxiv.org/abs/2312.03584) · — — Learns contextual correspondences across example image–text pairs and transfers them to a new generation query.
- **Kosmos-G: Generating Images in Context with Multimodal Large Language Models** — *ICLR 2024* · [paper: ICLR proceedings](https://proceedings.iclr.cc/paper_files/paper/2024/hash/b2fe1ee8d936ac08dd26f2ff58986c8f-Abstract-Conference.html) · [paper: arXiv:2310.02992](https://arxiv.org/abs/2310.02992) · [code](https://github.com/xichenpan/Kosmos-G) ✅ — Uses an MLLM to encode interleaved text and multiple images into an aligned context for compositional image generation.
- **MultiGen: Zero-shot Image Generation from Multi-modal Prompts** — *ECCV 2024* · [paper: ECCV](https://eccv.ecva.net/virtual/2024/poster/1503) · — — Combines several visual object exemplars, text, and optional coordinates in a zero-shot multi-object generation pipeline; no public arXiv record or official code was located.

## 2. Multi-subject and multi-identity personalization

This section focuses on preserving and spatially disentangling several referenced subjects or people in one generated image.

### 2026

- **PSR: Scaling Multi-Subject Personalized Image Generation with Pairwise Subject-Consistency Rewards** — *CVPR 2026* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2026/html/Wang_PSR_Scaling_Multi-Subject_Personalized_Image_Generation_with_Pairwise_Subject-Consistency_Rewards_CVPR_2026_paper.html) · [code](https://github.com/wang-shulei/PSR) ✅ — Introduces pairwise subject-consistency rewards and PSRBench to scale preference optimization beyond one personalized subject.
- **Scaling Multi-Identity Consistency for Image Customization via Multi-to-Multi Matching Paradigm** — *CVPR 2026* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2026/html/Cheng_Scaling_Multi-Identity_Consistency_for_Image_Customization_via_Multi-to-Multi_Matching_Paradigm_CVPR_2026_paper.html) · [paper: arXiv:2509.06818](https://arxiv.org/abs/2509.06818) · [project](https://bytedance.github.io/UMO/) · [code](https://github.com/bytedance/UMO) ✅ — UMO optimizes all generated and reference identities jointly through a multi-to-multi matching reward; its arXiv title begins “UMO:”.
- **MultiCrafter: High-Fidelity Multi-Subject Generation via Disentangled Attention and Identity-Aware Preference Alignment** — *CVPR 2026* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2026/html/Wu_MultiCrafter_High-Fidelity_Multi-Subject_Generation_via_Disentangled_Attention_and_Identity-Aware_Preference_CVPR_2026_paper.html) · [paper: arXiv:2509.21953](https://arxiv.org/abs/2509.21953) · [repository](https://github.com/WuTao-CS/MultiCrafter) 🧩 — Separates subject attention spatially and aligns identity preferences; the public repository contained documentation/assets but not the implementation at verification time.
- **MOSAIC: Multi-Subject Personalized Generation via Correspondence-Aware Alignment and Disentanglement** — *ICLR 2026* · [paper: OpenReview 7AH0y1OtnC](https://openreview.net/forum?id=7AH0y1OtnC) · [paper: arXiv:2509.01977](https://arxiv.org/abs/2509.01977) · [project](https://bytedance-fanqie-ai.github.io/MOSAIC/) · [code](https://github.com/bytedance-fanqie-ai/MOSAIC) ✅ — Aligns each reference with its prompt role and disentangles subject features to suppress identity leakage.
- **FocusDPO: Dynamic Preference Optimization for Multi-Subject Personalized Image Generation via Adaptive Focus** — *arXiv preprint, 2025; AAAI 2026 author-reported in the official repository* · [paper: arXiv:2509.01181](https://arxiv.org/abs/2509.01181) · [repository](https://github.com/bytedance-fanqie-ai/FocusDPO) 🧩 — Dynamically focuses preference optimization on whichever subject or relation currently fails; the repository promises code/model release.
- **Preserving Compositionality for Robust Multi-Subject Personalization in Text-to-Image Generation** — *UAI 2026, PMLR 337* · [paper: PMLR](https://proceedings.mlr.press/v337/lee26f.html) · — — Regularizes multi-subject personalization so learned identities remain composable under new prompts and layouts.
- **Hierarchical Concept-to-Appearance Guidance for Multi-Subject Image Generation** — *arXiv preprint, 2026* · [paper: arXiv:2602.03448](https://arxiv.org/abs/2602.03448) · — — CAG separates coarse concept assignment from fine appearance guidance to preserve multiple referenced subjects without cross-contamination.

### 2025

- **MUSE: Multi-Subject Unified Synthesis via Explicit Layout Semantic Expansion** — *ICCV 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/ICCV2025/html/Peng_MUSE_Multi-Subject_Unified_Synthesis_via_Explicit_Layout_Semantic_Expansion_ICCV_2025_paper.html) · [paper: arXiv:2508.14440](https://arxiv.org/abs/2508.14440) · [code](https://github.com/pf0607/MUSE) ✅ — Expands subject semantics into explicit layouts to improve identity retention and spatial control for several references.
- **XVerse: Consistent Multi-Subject Control of Identity and Semantic Attributes via DiT Modulation** — *NeurIPS 2025* · [paper: NeurIPS proceedings](https://papers.nips.cc/paper_files/paper/2025/file/0b0153a91f827b14e8bfea4e211362f3-Paper-Conference.pdf) · [paper: arXiv:2506.21416](https://arxiv.org/abs/2506.21416) · [project](https://bytedance.github.io/XVerse/) · [code](https://github.com/bytedance/XVerse) ✅ — Modulates a diffusion transformer to control several identities and their semantic attributes consistently.
- **Multi-party Collaborative Attention Control for Image Customization** — *CVPR 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2025/html/Yang_Multi-party_Collaborative_Attention_Control_for_Image_Customization_CVPR_2025_paper.html) · [paper: arXiv:2505.01428](https://arxiv.org/abs/2505.01428) · [code](https://github.com/yanghan-yh/MCA-Ctrl) ✅ — MCA-Ctrl coordinates attention among multiple reference parties to localize subjects and avoid feature leakage.
- **DreamO: A Unified Framework for Image Customization** — *arXiv preprint, 2025; SIGGRAPH Asia 2025 author-reported in the official repository* · [paper: arXiv:2504.16915](https://arxiv.org/abs/2504.16915) · [code](https://github.com/bytedance/DreamO) ✅ — A routed conditioning framework that combines multiple identities, subjects, garments, and other reference types in one image.
- **DynamicID: Zero-Shot Multi-ID Image Personalization with Flexible Facial Editability** — *ICCV 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/ICCV2025/html/Hu_DynamicID_Zero-Shot_Multi-ID_Image_Personalization_with_Flexible_Facial_Editability_ICCV_2025_paper.html) · [paper: arXiv:2503.06505](https://arxiv.org/abs/2503.06505) · [code](https://github.com/ByteCat-bot/DynamicID) ✅ — Preserves several facial identities zero-shot while retaining prompt-driven expression and attribute editability.
- **AnyStory: Towards Unified Single and Multiple Subject Personalization in Text-to-Image Generation** — *arXiv preprint, 2025* · [paper: arXiv:2501.09503](https://arxiv.org/abs/2501.09503) · [project](https://aigcdesigngroup.github.io/AnyStory/) · [code](https://github.com/junjiehe96/AnyStory) ✅ — Uses an encode-then-route design with instance-aware subject routing for both single- and explicit multi-reference subject personalization.
- **Resolving Multi-Condition Confusion for Finetuning-Free Personalized Image Generation** — *AAAI 2025* · [paper: AAAI proceedings](https://ojs.aaai.org/index.php/AAAI/article/view/32386) · [paper: arXiv:2409.17920](https://arxiv.org/abs/2409.17920) · [code](https://github.com/hqhQAQ/MIP-Adapter) ✅ — MIP-Adapter disentangles multiple image conditions to prevent one referenced subject from overriding another.
- **UniPortrait: A Unified Framework for Identity-Preserving Single- and Multi-Human Image Personalization** — *ICCV 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/ICCV2025/html/He_UniPortrait_A_Unified_Framework_for_Identity-Preserving_Single-_and_Multi-Human_Image_ICCV_2025_paper.html) · [paper: arXiv:2408.05939](https://arxiv.org/abs/2408.05939) · [project](https://aigcdesigngroup.github.io/UniPortrait-Page/) · [code](https://github.com/junjiehe96/UniPortrait) ✅ — Uses a unified identity representation and routing mechanism for one or several referenced people.
- **MS-Diffusion: Multi-subject Zero-shot Image Personalization with Layout Guidance** — *ICLR 2025* · [paper: OpenReview PJqP0wyQek](https://openreview.net/forum?id=PJqP0wyQek) · [paper: arXiv:2406.07209](https://arxiv.org/abs/2406.07209) · [project](https://ms-diffusion.github.io/) · [code](https://github.com/MS-Diffusion/MS-Diffusion) ✅ — Injects subject-specific visual tokens into bounded spatial regions and supplies MS-Bench for multi-subject evaluation.
- **TFCustom: Customized Image Generation with Time-Aware Frequency Feature Guidance** — *CVPR 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2025/html/Liu_TFCustom_Customized_Image_Generation_with_Time-Aware_Frequency_Feature_Guidance_CVPR_2025_paper.html) · — — Uses time-aware frequency guidance to balance prompt semantics and visual fidelity, including customized multi-object generation.
- **MultiBooth: Towards Generating All Your Concepts in an Image from Text** — *AAAI 2025* · [paper: AAAI proceedings](https://ojs.aaai.org/index.php/AAAI/article/view/33187) · [paper: arXiv:2404.14239](https://arxiv.org/abs/2404.14239) · [project](https://multibooth.github.io/) · [repository](https://github.com/chenyangzhu1/MultiBooth) 🧩 — Encodes and positions several user concepts jointly; the official repository still described code as forthcoming when checked.
- **FastComposer: Tuning-Free Multi-Subject Image Generation with Localized Attention** — *International Journal of Computer Vision 133, 2025* · [paper: Springer](https://link.springer.com/article/10.1007/s11263-024-02227-z) · [paper: arXiv:2305.10431](https://arxiv.org/abs/2305.10431) · [code](https://github.com/mit-han-lab/fastcomposer) ✅ — Encodes multiple people without per-user tuning and localizes their cross-attention to reduce identity blending.

### 2024

- **StoryMaker: Towards Holistic Consistent Characters in Text-to-image Generation** — *arXiv preprint, 2024* · [paper: arXiv:2409.12576](https://arxiv.org/abs/2409.12576) · [code and model](https://github.com/RedAIGC/StoryMaker) ✅ — Conditions on separate face and full-character references and prevents feature intermingling when generating scenes with multiple people.
- **Identity Decoupling for Multi-Subject Personalization of Text-to-Image Models** — *NeurIPS 2024* · [paper: NeurIPS proceedings](https://proceedings.neurips.cc/paper_files/paper/2024/hash/b6e67ae290635d0874c4cb43ba2a2cfb-Abstract-Conference.html) · [paper: arXiv:2404.04243](https://arxiv.org/abs/2404.04243) · [paper: OpenReview tEEpVPDaRf](https://openreview.net/forum?id=tEEpVPDaRf) · [code](https://github.com/agwmon/MuDI) ✅ — MuDI decouples identity embeddings and uses segmented generation data to compose several subjects with less identity mixing.
- **MM-Diff: High-Fidelity Image Personalization via Multi-Modal Condition Integration** — *arXiv preprint, 2024* · [paper: arXiv:2403.15059](https://arxiv.org/abs/2403.15059) · [project](https://mm-diff.github.io/) · [code](https://github.com/alibaba/mm-diff) ✅ — Integrates text, visual, and identity conditions and explicitly supports multiple references and identity mixing.
- **Subject-Diffusion: Open Domain Personalized Text-to-Image Generation without Test-time Fine-tuning** — *arXiv preprint, 2023; SIGGRAPH 2024 author-reported in the official repository* · [paper: arXiv:2307.11410](https://arxiv.org/abs/2307.11410) · [project](https://oppo-mente-lab.github.io/subject_diffusion/) · [code](https://github.com/OPPO-Mente-Lab/Subject-Diffusion) ✅ — Learns subject embeddings and location control from a large synthetic dataset, including generation with several referenced subjects.

### 2023

- **Cones 2: Customizable Image Synthesis with Multiple Subjects** — *NeurIPS 2023* · [paper: NeurIPS proceedings](https://proceedings.neurips.cc/paper_files/paper/2023/hash/b3847cda0c8cc0cfcdacf462dc122214-Abstract-Conference.html) · [paper: arXiv:2305.19327](https://arxiv.org/abs/2305.19327) · [code](https://github.com/ali-vilab/Cones-V2) ✅ — Learns lightweight subject residuals and composes several customized subjects through layout-aware guidance.

## 3. Multi-concept and content–style composition

These methods merge multiple learned concept modules or deliberately combine distinct content/style references.

### 2026

- **Unified Customized Generation by Disentangled Reward Modeling** — *CVPR 2026* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2026/html/Wu_Unified_Customized_Generation_by_Disentangled_Reward_Modeling_CVPR_2026_paper.html) · [paper: arXiv:2508.18966](https://arxiv.org/abs/2508.18966) · [project](https://bytedance.github.io/USO/) · [code and model](https://github.com/bytedance/USO) ✅ — Published as USO, it combines a subject/content reference with one or two style references and also supports multiple-style aggregation; the arXiv title is “USO: Unified Style and Subject-Driven Generation via Disentangled and Reward Learning.”
- **CRAFT-LoRA: Content-Style Personalization via Rank-Constrained Adaptation and Training-Free Fusion** — *CVPR 2026* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2026/html/Li_CRAFT-LoRA_Content-Style_Personalization_via_Rank-Constrained_Adaptation_and_Training-Free_Fusion_CVPR_2026_paper.html) · [paper: arXiv:2602.18936](https://arxiv.org/abs/2602.18936) · [code](https://github.com/Skylanding/CraftLoRA) ✅ — Learns rank-constrained content and style LoRAs that can be fused at inference without joint retraining.

### 2025

- **CSGO: Content-Style Composition in Text-to-Image Generation** — *NeurIPS 2025* · [paper: NeurIPS proceedings](https://papers.neurips.cc/paper_files/paper/2025/hash/9144c7c014bf4c30e88f650bef8f68dd-Abstract-Conference.html) · [paper: arXiv:2408.16766](https://arxiv.org/abs/2408.16766) · [project](https://csgo-gen.github.io/) · [code](https://github.com/instantX-research/CSGO) ✅ — Independently injects a content image and a style image, trained on the 210K-triplet IMAGStyle dataset, for explicit two-reference composition.
- **AIComposer: Any Style and Content Image Composition via Feature Integration** — *ICCV 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/ICCV2025/html/Li_AIComposer_Any_Style_and_Content_Image_Composition_via_Feature_Integration_ICCV_2025_paper.html) · [paper: arXiv:2507.20721](https://arxiv.org/abs/2507.20721) · [code](https://github.com/sherlhw/AIComposer) ✅ — Integrates multiple foreground, background, content, and style reference features in a single controlled composition.
- **Cached Multi-Lora Composition for Multi-Concept Image Generation** — *ICLR 2025* · [paper: OpenReview 4iFSBgxvIO](https://openreview.net/forum?id=4iFSBgxvIO) · [paper: arXiv:2502.04923](https://arxiv.org/abs/2502.04923) · [code](https://github.com/YqcCa/CMLoRA) ✅ — Caches and selectively composes multiple LoRA features, limiting concept interference without joint training.
- **MC²: Multi-concept Guidance for Customized Multi-concept Generation** — *CVPR 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2025/html/Jiang_MC2_Multi-concept_Guidance_for_Customized__Multi-concept_Generation_CVPR_2025_paper.html) · [paper: arXiv:2404.05268](https://arxiv.org/abs/2404.05268) · [code](https://github.com/JIANGJiaXiu/MC-2) ✅ — Adds inference-time concept-specific guidance and the MC++ benchmark to reduce omission and attribute leakage.
- **LoRA-Composer: Leveraging Low-Rank Adaptation for Multi-Concept Customization in Training-Free Diffusion Models** — *IEEE Transactions on Image Processing, 2025, as reported by the official repository* · [paper: arXiv:2403.11627](https://arxiv.org/abs/2403.11627) · [code](https://github.com/Young98CN/LoRA_Composer) ✅ — Coordinates independently trained LoRAs with concept-region constraints and inference-time attention manipulation.

### 2024

- **Concept Conductor: Orchestrating Multiple Personalized Concepts in Text-to-Image Synthesis** — *arXiv preprint, 2024* · [paper: arXiv:2408.03632](https://arxiv.org/abs/2408.03632) · [code](https://github.com/Nihukat/Concept-Conductor) ✅ — Orchestrates several personalized models with layout-guided sampling and concept-specific latent fusion.
- **FreeCustom: Tuning-Free Customized Image Generation for Multi-Concept Composition** — *CVPR 2024* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2024/html/Ding_FreeCustom_Tuning-Free_Customized_Image_Generation_for_Multi-Concept_Composition_CVPR_2024_paper.html) · [paper: arXiv:2405.13870](https://arxiv.org/abs/2405.13870) · [code](https://github.com/aim-uofa/FreeCustom) ✅ — Composes multiple reference concepts at inference by extracting and injecting multiscale visual features, without tuning.
- **Concept Weaver: Enabling Multi-Concept Fusion in Text-to-Image Models** — *CVPR 2024* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2024/html/Kwon_Concept_Weaver_Enabling_Multi-Concept_Fusion_in_Text-to-Image_Models_CVPR_2024_paper.html) · [paper: arXiv:2404.03913](https://arxiv.org/abs/2404.03913) · [official publication page](https://research.adobe.com/publication/concept-weaver-enabling-multi-concept-fusion-in-text-to-image-models/) 🧩 — Fuses several personalized concept models through concept-specific denoising paths and mask-guided composition.
- **DEADiff: An Efficient Stylization Diffusion Model with Disentangled Representations** — *CVPR 2024* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2024/html/Qi_DEADiff_An_Efficient_Stylization_Diffusion_Model_with_Disentangled_Representations_CVPR_2024_paper.html) · [paper: arXiv:2403.06951](https://arxiv.org/abs/2403.06951) · [project](https://tianhao-qi.github.io/DEADiff/) · [code](https://github.com/bytedance/DEADiff) ✅ — Its disentangled style encoder supports mixing styles from multiple reference images and can pair a style reference with ControlNet structural content.
- **OMG: Occlusion-friendly Personalized Multi-concept Generation in Diffusion Models** — *ECCV 2024* · [paper: ECCV](https://eccv.ecva.net/virtual/2024/poster/1768) · [paper: arXiv:2403.10983](https://arxiv.org/abs/2403.10983) · [code](https://github.com/kongzhecn/OMG) ✅ — Uses an occlusion-aware layout-to-image stage followed by concept injection for interacting or partially hidden subjects.
- **Implicit Style-Content Separation using B-LoRA** — *ECCV 2024* · [paper: arXiv:2403.14572](https://arxiv.org/abs/2403.14572) · [code](https://github.com/yardenfren1996/B-LoRA) ✅ — Learns separate low-rank blocks for content and style, enabling one content reference to be rendered in another reference's style.
- **Multi-LoRA Composition for Image Generation** — *Transactions on Machine Learning Research, 2024* · [paper: OpenReview 25FT0DqhVZ](https://openreview.net/forum?id=25FT0DqhVZ) · [paper: arXiv:2402.16843](https://arxiv.org/abs/2402.16843) · [project](https://maszhongming.github.io/Multi-LoRA-Composition/) · [code](https://github.com/maszhongming/Multi-LoRA-Composition) ✅ — Composes independently learned concept LoRAs and introduces ComposLoRA for measuring multi-concept fidelity.
- **λ-ECLIPSE: Multi-Concept Personalized Text-to-Image Diffusion Models by Leveraging CLIP Latent Space** — *Transactions on Machine Learning Research, 2024* · [paper: OpenReview 7q5UewlAdM](https://openreview.net/forum?id=7q5UewlAdM) · [paper: arXiv:2402.05195](https://arxiv.org/abs/2402.05195) · [project](https://eclipse-t2i.github.io/Lambda-ECLIPSE/) · [code](https://github.com/eclipse-t2i/lambda-eclipse-inference) ✅ — Predicts personalized CLIP-space priors and combines several concepts without fine-tuning the diffusion backbone.
- **ZipLoRA: Any Subject in Any Style by Effectively Merging LoRAs** — *ECCV 2024* · [paper: ECCV](https://eccv.ecva.net/virtual/2024/poster/1760) · [paper: arXiv:2311.13600](https://arxiv.org/abs/2311.13600) · [project](https://ziplora.github.io/) 🧩 — Merges independently trained subject and style LoRAs by encouraging sparse, disjoint parameter changes.

### 2023

- **Mix-of-Show: Decentralized Low-Rank Adaptation for Multi-Concept Customization of Diffusion Models** — *NeurIPS 2023* · [paper: NeurIPS proceedings](https://proceedings.neurips.cc/paper_files/paper/2023/hash/3340ee1e4a8bad8d32c35721712b4d0a-Abstract-Conference.html) · [paper: arXiv:2305.18292](https://arxiv.org/abs/2305.18292) · [code](https://github.com/TencentARC/Mix-of-Show) ✅ — Trains concepts independently and fuses their low-rank updates into a regional multi-concept composition model.
- **Break-A-Scene: Extracting Multiple Concepts from a Single Image** — *ACM SIGGRAPH Asia 2023* · [paper: DOI 10.1145/3610548.3618154](https://doi.org/10.1145/3610548.3618154) · [paper: arXiv:2305.16311](https://arxiv.org/abs/2305.16311) · [project](https://omriavrahami.com/break-a-scene/) · [code](https://github.com/google/break-a-scene) ✅ — Extracts several independently reusable concept tokens from one image, directly enabling later recombination.
- **Multi-Concept Customization of Text-to-Image Diffusion** — *CVPR 2023* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2023/html/Kumari_Multi-Concept_Customization_of_Text-to-Image_Diffusion_CVPR_2023_paper.html) · [paper: arXiv:2212.04488](https://arxiv.org/abs/2212.04488) · [project](https://www.cs.cmu.edu/~custom-diffusion/) · [code](https://github.com/adobe-research/custom-diffusion) ✅ — Custom Diffusion established efficient joint and post-hoc composition of multiple personalized concepts.

## 4. Multiple-image aggregation for one identity or concept

These methods use a *set* of images to infer a shared identity/style/subject representation; they are multi-reference even when the output contains only one personalized subject.

### 2025

- **EasyRef: Omni-Generalized Group Image Reference for Diffusion Models via Multimodal LLM** — *ICML 2025* · [paper: OpenReview GNTmqRTpzr](https://openreview.net/forum?id=GNTmqRTpzr) · [paper: arXiv:2412.09618](https://arxiv.org/abs/2412.09618) · [code](https://github.com/TempleX98/EasyRef) ✅ — Uses an MLLM to aggregate a group of reference images into a shared identity, object, or style condition and introduces MRBench.
- **Generating Multi-Image Synthetic Data for Text-to-Image Customization** — *ICCV 2025* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/ICCV2025/html/Kumari_Generating_Multi-Image_Synthetic_Data_for_Text-to-Image_Customization_ICCV_2025_paper.html) · [paper: arXiv:2502.01720](https://arxiv.org/abs/2502.01720) · [project](https://www.cs.cmu.edu/~syncd-project/) · [code](https://github.com/nupurkmr9/syncd) ✅ — SynCD synthesizes consistent multi-image subject sets and trains customization models to aggregate identity evidence across views.

### 2024

- **PhotoMaker: Customizing Realistic Human Photos via Stacked ID Embedding** — *CVPR 2024* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2024/html/Li_PhotoMaker_Customizing_Realistic_Human_Photos_via_Stacked_ID_Embedding_CVPR_2024_paper.html) · [paper: arXiv:2312.04461](https://arxiv.org/abs/2312.04461) · [project](https://photo-maker.github.io/) · [code](https://github.com/TencentARC/PhotoMaker) ✅ — Stacks an arbitrary number of same-person references into a robust identity embedding and also supports identity mixing.
- **InstantBooth: Personalized Text-to-Image Generation without Test-Time Finetuning** — *CVPR 2024* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2024/html/Shi_InstantBooth_Personalized_Text-to-Image_Generation_without_Test-Time_Finetuning_CVPR_2024_paper.html) · [paper: arXiv:2304.03411](https://arxiv.org/abs/2304.03411) · — — Encodes a set of one or more images into global concept and local patch features, making it an early multi-image aggregation method for one personalized concept.

## 5. Dedicated benchmarks and datasets

### 2026

- **TRACE-Bench: Decomposing and Diagnosing Multi-Reference Image Generation** — *arXiv preprint, 2026* · [paper: arXiv:2608.16765](https://arxiv.org/abs/2608.16765) · [project](https://amuseum-whr.github.io/TraceBench/) 🧩 — Decomposes multi-reference fidelity into diagnostic dimensions instead of collapsing performance into one similarity score.
- **CogCanvas: A Benchmark for Evaluating Multi-Subject Reference-Based Image Generation** — *arXiv preprint, 2026* · [paper: arXiv:2606.15867](https://arxiv.org/abs/2606.15867) · — — Stress-tests reference-based generation across multiple subjects, relations, and compositional scenes.
- **When Identities Collapse: A Stress-Test Benchmark for Multi-Subject Personalization** — *arXiv preprint, 2026* · [paper: arXiv:2603.26078](https://arxiv.org/abs/2603.26078) · — — Targets identity collision and cross-subject leakage under difficult multi-person conditions.
- **MICON-Bench: Benchmarking and Enhancing Multi-Image Context Image Generation in Unified Multimodal Models** — *arXiv preprint, 2026* · [paper: arXiv:2602.19497](https://arxiv.org/abs/2602.19497) · [code and benchmark](https://github.com/Angusliuuu/MICON-Bench) ✅ — Evaluates unified multimodal models on generation that requires jointly reasoning over several context images.
- **MultiBanana: A Challenging Benchmark for Multi-Reference Text-to-Image Generation** — *CVPR 2026* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2026/html/Oshima_MultiBanana_A_Challenging_Benchmark_for_Multi-Reference_Text-to-Image_Generation_CVPR_2026_paper.html) · [paper: arXiv:2511.22989](https://arxiv.org/abs/2511.22989) · [code and data](https://github.com/matsuolab/multibanana) ✅ — Provides 3,769 tasks with as many as eight references and evaluates identity, attribute, relation, and overall instruction faithfulness.

### 2025

- **MultiRef: Controllable Image Generation with Multiple Visual References** — *ACM Multimedia 2025 Dataset Track* · [paper: OpenReview RRke9yXm1x](https://openreview.net/forum?id=RRke9yXm1x) · [paper: arXiv:2508.06905](https://arxiv.org/abs/2508.06905) · [project and data](https://multiref.github.io/) 🧩 — Contributes a 38K-example multi-reference dataset and a 1,990-example benchmark spanning subjects, styles, and spatial controls.

### Benchmarks bundled with method papers

| Benchmark | Introduced by | Primary focus |
|---|---|---|
| OmniRef-Bench | DyRef | Dynamic difficulty across multi-reference subject, attribute, and relation fidelity |
| MacroBench | MACRO | Long-context generation with as many as ten references |
| MSP-Bench | MultiCompose | Per-subject attribute binding in multi-concept scenes |
| MSIC | MUSIC | Multi-subject in-context generation and reasoning |
| PSRBench | PSR | Scalable multi-subject personalization and pairwise consistency |
| MRBench | EasyRef | Group-reference aggregation across identity, object, and style |
| MS-Bench | MS-Diffusion | Multi-subject identity and layout fidelity |
| MC++ | MC² | Customized multi-concept composition |
| ComposLoRA | Multi-LoRA Composition | Composition of independently trained LoRAs |

## 6. Background foundations — not counted as direct multi-reference papers

These papers are important building blocks, but their primary problem setting is single-subject or single-reference personalization. They are intentionally separated from the main bibliography.

- **IP-Adapter: Text Compatible Image Prompt Adapter for Text-to-Image Diffusion Models** — *arXiv technical report, 2023* · [paper: arXiv:2308.06721](https://arxiv.org/abs/2308.06721) · [project](https://ip-adapter.github.io/) · [code](https://github.com/tencent-ailab/IP-Adapter) ✅ — A decoupled image-prompt adapter reused by many later zero-shot multi-reference systems.
- **BLIP-Diffusion: Pre-trained Subject Representation for Controllable Text-to-Image Generation and Editing** — *NeurIPS 2023* · [paper: NeurIPS proceedings](https://proceedings.neurips.cc/paper_files/paper/2023/hash/602e1a5de9c47df34cae39353a7f5bb1-Abstract-Conference.html) · [paper: arXiv:2305.14720](https://arxiv.org/abs/2305.14720) · [code](https://github.com/salesforce/LAVIS/tree/main/projects/blip-diffusion) ✅ — Pretrains a general subject representation that inspired later multi-subject conditioning architectures.
- **DreamBooth: Fine Tuning Text-to-Image Diffusion Models for Subject-Driven Generation** — *CVPR 2023* · [paper: CVF Open Access](https://openaccess.thecvf.com/content/CVPR2023/html/Ruiz_DreamBooth_Fine_Tuning_Text-to-Image_Diffusion_Models_for_Subject-Driven_Generation_CVPR_2023_paper.html) · [paper: arXiv:2208.12242](https://arxiv.org/abs/2208.12242) · [project](https://dreambooth.github.io/) 🧩 — Established few-image subject-driven diffusion fine-tuning, the baseline from which much multi-subject personalization evolved.
- **An Image is Worth One Word: Personalizing Text-to-Image Generation using Textual Inversion** — *ICLR 2023* · [paper: OpenReview 3L2mUQ2pf0](https://openreview.net/forum?id=3L2mUQ2pf0) · [paper: arXiv:2208.01618](https://arxiv.org/abs/2208.01618) · [code](https://github.com/rinongal/textual_inversion) ✅ — Introduced learned placeholder tokens for visual concepts, a foundation for later multi-token and multi-concept composition.

## Maintenance

Additions and corrections follow the shared
[contribution guide](../CONTRIBUTING.md) and
[maintenance checklist](../.github/MAINTAINING.md).
