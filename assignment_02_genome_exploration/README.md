# Genome Exploration II — Spatula clypeata

## Species and Genome Information

- **Species:** *Spatula clypeata*
- **NCBI Assembly accession:** GCA_977066335.1
- **Assembly level:** Contig / Scaffold
- **FASTA file:** Spatula_clypeata_genomic.fna
- **Genome source:** NCBI
- **Approximate file size:** 1.3 GB

## Objective

The objective of this activity was to examine the basic structure and sequence characteristics of the *Spatula clypeata* genome using NCBI and Galaxy. The analysis included generating assembly statistics, examining sequence lengths, filtering sequences by length, and exploring possible open reading frames (ORFs).

## Galaxy Analysis

### 1. Assembly Statistics

The Galaxy tools **gfastats** and **FASTA Statistics** were used to examine the genome assembly.

The original assembly showed:

| Metric | Scaffold | Contigs |
|---|---:|---:|
| Total assembly length | 1,236,977,220 bp | 1,236,883,420 bp |
| Number of sequences | 538 | 1,007 |
| Minimum sequence length | 1,000 bp | 1,000 bp |
| Maximum sequence length | 206,960,320 bp | 15,897,514 bp |
| Mean sequence length | 2,299,214.16 bp | 1,228,285.42 bp |
| N50 | 76,684,505 bp | 3,649,032 bp |
| L50 | 5 | 100 |
| GC content | 42.26% | 42.26% |

### 2. Sequence-Length Structure

The **Compute Sequence Length** tool was used to determine the length of individual sequences.

The five longest scaffold sequences were:

1. OZ370056.1 — 206,960,320 bp
2. OZ370057.1 — 159,235,870 bp
3. OZ370058.1 — 119,292,994 bp
4. OZ370059.1 — 76,684,505 bp
5. OZ370060.1 — 64,834,719 bp


### 3. 10 kb Filtering Experiment

The **Filter Sequences by Length** tool was used with a minimum sequence length of **10,000 bp**.

After filtering:

| Metric | Scaffold | Contigs |
|---|---:|---:|
| Total length | 1,236,922,307 bp | 1,236,828,507 bp |
| Number of sequences | 512 | 981 |
| Maximum length | 206,960,320 bp | 15,897,514 bp |
| N50 | 76,684,505 bp | 3,649,032 bp |
| GC content | 42.25% | 42.25% |

The filter removed **26 scaffold sequences and 26 contig sequences**. The total assembly length decreased only slightly, and the N50 remained the same. This indicates that the removed short sequences contributed relatively little to the total assembly length, although they may still contain real biological information.

### 4. ORF Exploration

The **Filter sequences by ID** tool was first used to select the sequence for ORF analysis. The selected sequence was from the *Spatula clypeata* genome assembly, contig HAP1_SCAFFOLD_17.

The **getorf** tool was then used with a minimum ORF size of **300 bp**.

The analysis found:

- **Number of ORFs:** 428
- **Longest ORF:** CDRUPU010000026.1_358 [47191–430671]
- **Strand:** Reverse sense
- **ORF length:** 1,375 bp

Not every ORF should be reported as a real gene because an ORF only represents a potential protein-coding region. Some ORFs can occur by chance, so additional evidence such as similarity to known genes or proteins and gene annotation is needed to confirm that an ORF represents a real gene.

## Biological Interpretation

The *Spatula clypeata* genome assembly appears relatively well assembled based on the large scaffold N50 and long scaffold sequences. The scaffold N50 of 76.7 Mb and L50 of 5 indicate that a small number of large scaffolds make up a large part of the genome. The maximum scaffold length is about 207 Mb. In comparison, the contig N50 of about 3.65 Mb and L50 of 100 indicate that the contig-level assembly is more fragmented.

The 10 kb filtering experiment showed that short sequences contributed relatively little to the total genome size because removing them only slightly reduced the total assembly length. However, this does not mean that the filtered assembly is automatically better because short sequences may still contain real biological information. The genome has a GC content of about 42.3%. The ORF analysis demonstrated that a genome sequence can contain many possible coding regions, but these ORFs should not automatically be considered real genes because additional evidence is needed to confirm their function.
