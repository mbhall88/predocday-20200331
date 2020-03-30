+++
weight = 5
+++
{{% section %}}

## Evaluation

---

### Simulated data

Aim to show that the addition of *de novo* discovery allows `pandora` to improve its
ability to discover and call variants correctly (precision/recall).

---

### Simulated data

-   100 local PRGs (genes)
-   Random path from each joined together into a genome
-   Introduce variants at a given rate
-   Simulate Nanopore reads from mutated genome
-   Run `pandora` with reads from mutated genome
-   Assess how many introduced variants were found

---

### Assessing variants

<img src="images/evaluation.png"  height="520" width="1000" style="border: none;">

---

### Simulation results

<img src="images/simulations.png"  height="550" width="1000" style="border: none;">

---

## Empirical data

-   The main focus of both `pandora` and *de novo* evaluation
-   Use `compare` routine to show the power of the reference-graph approach
-   4 *E. coli* samples from different phylogroups
-   Compare to variant caller `snippy` - using a variety of references (~250)

---

## Empirical data

Difficulty in evaluating four-way is "truth"

-   Align each pair of genomes with `nucmer` to get differences
-   Construct truth panel from these differences
-   Map truth panel to a panel of probes from `pandora` VCF
-   Calculate recall and precision for all pairs

---

### Results - Illumina

<img src="images/results-illumina.png"  height="600" width="1100" style="border: none;">

---

### Results - Nanopore

<img src="images/results-nanopore.png"  height="600" width="1100" style="border: none;">

---

### Results - Both

<img src="images/results-all.png"  height="600" width="1100" style="border: none;">

---

## Outstanding work

-   Re-evaluation of four-way with methylation-aware nanopore basecalling
-   Scaling evaluation to 26 samples from across the *E. coli* tree
-   Direct integration of *de novo* variants back into PRG
-   100-way analysis to validate the limit in variant detection using single-reference approaches


{{% /section %}}
