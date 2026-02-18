# Exercise 2: Biological Interpretation & Cell Phenotyping

Now that you’ve mastered the technical aspects of image viewing, we will apply these skills to a real-world clinical sample: a **Lung Cancer specimen** imaged via Cyclic Immunofluorescence (CyCIF).

## The Data

We will use the interactive viewer for the [Lung Adenocarcinoma (LUNG-3) dataset](https://www.cycif.org/data/du-lin-rashid-nat-protoc-2019/osd-LUNG_3#s=0#w=0#g=0#m=-1#a=-100_-100#v=1_0.6508_0.5#o=-100_-100_1_1#p=Q).

**Task:** Click the link above and follow the **"Step-by-Step Tour"** (the narrative panel on the left). As you go, answer the following questions.

---

## Part 1: Cell Morphology & Lineage

Spatial proteomics allows us to distinguish cells not just by *what* they express, but by *how they look*.

* **Cancer Cells vs. Immune Cells:** Look at the **Cytokeratin (CK)** markers vs. the **CD45/CD3/CD8** markers.
  * Compare the size of a Cytokeratin-positive epithelial cell to a CD3-positive Lymphocyte.
  * **Question:** Which cell type typically has a higher cytoplasm-to-nucleus ratio?

* **The Scale Bar:** Using the scale bar, estimate the diameter of a typical Lymphocyte in this tissue.

---

## Part 2: Subcellular Localization & Marker Logic

Markers are often categorized by **where** they show up in the cell and **what** they tell us about the cell's identity.

| Category | Definition | Example from this dataset |
| :--- | :--- | :--- |
| **Nuclear** | Stains the DNA or proteins within the nucleus. | DNA (Hoechst/DAPI), PCNA |
| **Cytoplasmic** | Stains the main body/structural proteins of the cell. | Cytokeratin, Vimentin |
| **Membranous** | Stains the outer boundary of the cell. | CD3, CD8, PD-L1 |

**Task:** Identify one marker in this image that is purely **Nuclear** and one that is purely **Membranous**.

---

## Part 3: Lineage vs. Functional Markers

* **Lineage Markers:** Tell us *what the cell is* (e.g., "I am a T-cell").
* **Functional Markers:** Tell us *what the cell is doing* (e.g., "I am exhausted" or "I am proliferating").

**Question:** Is **Ki67** (a marker of cell division) a lineage marker or a functional marker? Why?

---

## The "Real World" Challenge: Signal Aggregation

Navigate to the **"Cytotoxic T-cells"** tab and zoom in on a dense cluster of CD8/CD3 positive cells.

:::{admonition} BONUS: The Segmentation Headache
:class: danger
When cells are tightly packed or "aggregated," their signals often overlap.

1. How does this make **Single-Cell Segmentation** (drawing a boundary around each cell) difficult?
2. If two cells are touching, and the signal from one bleeds into the other, how might this lead to "False Positives" in your phenotyping?
:::

---

## Summary of Findings

Before finishing, reflect on how changing the "Min/Max" intensity (from Exercise 1) might change your opinion on whether a cell is "Positive" or "Negative" for a marker like PD-L1.
