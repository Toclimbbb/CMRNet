# CMRNet: A Multispectral Detection Framework Driven by Dynamic Intelligence for Coastal Environments

Welcome to the official repository for **CMRNet**.

## 📢 Update
**[Under Review]** The manuscript is currently undergoing the peer-review process. 

To comply with double-blind review policies and protect intellectual property prior to publication, the source code, pre-trained weights, and the **SeaRGBT-Tiny dataset** are temporarily withheld.

**We commit to making the complete training pipeline, inference code, and dataset fully public right here immediately upon the acceptance of the paper.**

---

## 📅 Release Roadmap
- [x] Release abstract and core performance metrics.
- [ ] Release the **SeaRGBT-Tiny** dataset (images and bounding box annotations).
- [ ] Release the core network components (MCDF, PolyBlock, DGQS).
- [ ] Release the complete training and evaluation pipeline.
- [ ] Release pre-trained weights for all tested benchmarks.

---

## 📖 Abstract
The complementarity of visible (RGB) and thermal infrared (TIR) features is crucial in maritime monitoring and perception, especially in coastal environments characterized by complex lighting and weather factors. However, mainstream existing multispectral feature fusion methods rely on static fusion strategies, which cannot adapt to rapid changes in modality reliability, causing cross-modal feature contamination and redundant computation over large backgrounds. 

To address these issues, this paper proposes a highly efficient and dynamically intelligent multispectral detection framework called CMRNet. Specifically, to tackle cross-modal feature contamination during fusion, we design modality complementary differential feature fusion, a new fusion paradigm inspired by common-mode rejection in differential amplifiers. By explicitly modeling modal differential potential energy, it builds dynamic reliability allocation and suppresses heterogeneous noise propagation. Considering the spatial redundancy of unstructured sea surfaces, we design a polymorphic convblock that routes computation according to scene complexity, allocating network capacity to complex regions. Furthermore, to prevent tiny objects from being overwhelmed by vast backgrounds, we design a spatial density prior to guide query selection toward potential targets. 

Experiments on SeaRGBT-Tiny, MSRS, FLIR, and LLVIP show that our method achieves excellent performance. On SeaRGBT-Tiny, it obtains **51.9% AP (+6.0%)**, requiring only **3.60M parameters and 3.01ms latency**.

---

## 🖼️ Architecture overview
*(Upload your architecture diagram to the repository and link it here)*

<details>
<summary>Click to view the overall architecture of CMRNet</summary>

![CMRNet Architecture](architecture.png) 
*CMRNet adopts an edge-deployable, dual-to-single progressive architecture for optimal balance between cross-modal interaction and computational efficiency.*
</details>

---

## 🚀 Main Results 
*Note: Latency is measured on the NVIDIA Jetson Orin Nano platform to verify real-time edge deployment capabilities.*

| Dataset | Model | AP (%) | Params (M) | Latency (ms) |
| :--- | :---: | :---: | :---: | :---: |
| **SeaRGBT-Tiny** | CMRNet (Ours) | **51.9** | **3.60** | **3.01** |
| MSRS | CMRNet (Ours) | - | 3.60 | 3.01 |
| FLIR | CMRNet (Ours) | - | 3.60 | 3.01 |

*(Please wait for the full update after acceptance for detailed quantitative and qualitative results.)*

---
*Stay tuned for updates!*
