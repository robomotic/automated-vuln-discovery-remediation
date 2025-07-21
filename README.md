

# Comprehensive Survey of Software Vulnerability Datasets with Realistic CVE Fixes

Based on extensive research across academic papers, repositories, and vulnerability databases, I have identified **15 major datasets** that contain realistic software vulnerabilities (CVEs) along with their corresponding fixes. These datasets are essential resources for security research, vulnerability detection model training, and automated program repair.

![Top 10 Vulnerability Datasets by Scale - Shows the number of vulnerabilities/CVEs in the largest available datasets](https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/be9ddc41e27e034d060bc5a45b9b8341/a4be58e9-4522-4fc2-965a-9ef55b609449/138e1eb1.png)

Top 10 Vulnerability Datasets by Scale - Shows the number of vulnerabilities/CVEs in the largest available datasets

## Most Comprehensive and Current Datasets

### 1. **MoreFixes** (2024) - *Largest Available*

MoreFixes represents the most comprehensive vulnerability dataset currently available, containing **26,617 unique CVEs** from **6,945 GitHub projects** with **31,883 unique fix commits**[1][2]. This dataset achieves a 397% increase in CVEs and 295% increase in covered projects compared to prior work, making it the definitive resource for large-scale vulnerability research.

**Key Features:**

- Programming language-independent coverage
- Enhanced repository discovery methodology
- Comprehensive metadata including CWEs, repository data, and method changes
- Available as 14GB PostgreSQL database with patch files
- **Access:** [GitHub](https://github.com/JafarAkhondali/Morefixes) | [Zenodo](https://zenodo.org/records/11199120)


### 2. **CVEfixes** (2024) - *Most Established*

CVEfixes is a well-established, continuously updated dataset containing **11,873 CVEs** with **12,107 vulnerability fixing commits** across **4,249 open-source projects**[3][4]. The latest version (v1.0.8) covers vulnerabilities up to July 2024 and spans 272 different CWE types.

**Key Features:**

- Multi-language support (C/C++, Java, Python, JavaScript, etc.)
- Automated collection pipeline from NVD and GitHub
- Relational database structure with detailed metadata
- 138,974 functions with before/after fix versions
- **Access:** [GitHub](https://github.com/secureIT-project/CVEfixes) | [Zenodo](https://zenodo.org/records/4476563)


### 3. **MegaVul** (2024) - *Most Comprehensive C/C++*

MegaVul provides **17,380 vulnerabilities** from **992 repositories** spanning **169 different vulnerability types**[5][6]. This dataset focuses specifically on C/C++ code and includes comprehensive code representations with multiple transformation formats.

**Key Features:**

- Covers vulnerabilities from January 2006 to October 2023
- Four different code representations for each vulnerability
- JSON format for easy integration
- Continuously updated with new discoveries


### 4. **DiverseVul** (2023) - *Most Diverse*

DiverseVul contains **18,945 vulnerable functions** and **330,492 non-vulnerable functions** extracted from **7,514 commits**, covering **150 CWEs**[7][8]. This dataset emphasizes diversity with coverage of **295 new projects** not found in previous datasets.

**Key Features:**

- Most diverse project coverage among all datasets
- High-quality labels with 60% accuracy (24% higher than combined BigVul/CrossVul/CVEfixes)
- Real-world vulnerabilities from security issue websites
- **Access:** [GitHub](https://github.com/wagner-group/diversevul)


## Specialized and Historical Datasets

### 5. **PatchDB** (2021) - *Security-Focused*

PatchDB provides approximately **12,000 security patches** and **24,000 non-security patches** from real-world projects[9]. This dataset specifically focuses on distinguishing security-relevant patches from general bug fixes.

**Access:** [Website](https://sunlab-gmu.github.io/PatchDB/)

### 6. **CrossVul** (2021) - *Multi-Language*

CrossVul is unique in covering **40+ programming languages** with **5,131 CVEs** and **27,476 files** (vulnerable and patched versions)[10][11]. This cross-language approach makes it valuable for polyglot vulnerability research.

**Access:** [Zenodo](https://zenodo.org/records/4734050)

### 7. **D2A** (2021) - *Differential Analysis*

D2A employs a novel differential analysis approach, comparing before-fix and after-fix versions to label vulnerabilities more accurately[12][13]. This methodology reduces false positives common in static analysis-based labeling.

**Access:** [GitHub](https://github.com/IBM/D2A) | [Website](https://ibm.github.io/D2A/)

### 8. **VulnPatchPairs** (2024) - *Paired Functions*

VulnPatchPairs provides **13,100 vulnerable functions** with their **13,100 patched counterparts**, focusing specifically on paired analysis for vulnerability detection research[14][15].

**Access:** [GitHub](https://github.com/niklasrisse/VPP)

## Classic Research Datasets

### 9. **BigVul** (2020) - *MSR Benchmark*

BigVul contains **3,754 vulnerabilities** from open-source GitHub projects and remains widely used in vulnerability detection research[16][17].

### 10. **Devign** (2019) - *Graph Neural Networks*

Devign includes **26,037 functions** (11,888 vulnerable) from four major C projects: Linux, FFmpeg, Qemu, and Wireshark[18][19][20]. This dataset pioneered graph-based vulnerability detection approaches.

**Access:** [Website](https://sites.google.com/view/devign)

### 11. **SARD/Juliet** (Continuous) - *NIST Standard*

The Software Assurance Reference Dataset maintains **450,000+ test cases** covering **150+ CWE classes** in multiple languages[21][22]. While including synthetic cases, it provides comprehensive coverage of vulnerability types.

**Access:** [NIST SARD](https://samate.nist.gov/SARD/)

### 12. **ReVeal** (2020) - *Real-World Focus*

ReVeal provides **18,169 functions** (1,664 vulnerable) from Chromium and Debian security trackers, emphasizing real-world applicability[23][24].

### 13. **VulDeePecker** (2018) - *Deep Learning Pioneer*

VulDeePecker was the first dataset designed for deep learning approaches, containing **61,638 code gadgets** with detailed vulnerability patterns[25][26][27].

### 14. **SySeVR** (2018) - *Semantic Analysis*

SySeVR provides **420,627 SeVCs** (Semantics-based Vulnerability Candidates) focusing on semantic relationships in vulnerable code[28][29].

### 15. **ICVul** (2025) - *Latest with VCCs*

ICVul represents the newest addition, featuring comprehensive metadata including Vulnerability-Contributing Commits (VCCs) with enhanced labeling reliability[30][31].

### 16. **SecurityEval** (2022) - *Code Generation Security Evaluation*

SecurityEval is a specialized evaluation dataset designed to assess the security of machine learning-based code generation techniques[^4]. This dataset contains **130 samples covering 75 vulnerability types** (CWEs) in Python, specifically formatted as prompts for code generation models[^4].

**Key Features:**

- **130 Python samples** across **75 distinct CWE types**[^4]
- Prompts designed for evaluating ML-based code generation security[^4]
- Each sample includes prompt and corresponding insecure code example[^4]
- Updated version contains **121 prompts for 69 CWEs**[^4]
- Available in JSONL format with unique identifiers[^4]
- **Access:** [GitHub](https://github.com/s2e-lab/SecurityEval)[^4] | [Hugging Face](https://huggingface.co/datasets/s2e-lab/SecurityEval)[^5]

**Dataset Structure:**

- `ID`: Unique identifier with format {CWE-ID}_{Source}_{Serial}.py[^4]
- `Prompt`: Partial source code for code generation input[^4]
- `Insecure_code`: Example vulnerable code that may be generated[^4]

**Purpose:** SecurityEval specifically targets the evaluation of automatically generated code for security vulnerabilities, making it unique among vulnerability datasets that typically focus on detection rather than generation assessment[^4].

This completes the comprehensive collection with all five datasets you specified. SecurityEval fills an important niche by focusing on the security evaluation of AI-generated code, complementing the other datasets which primarily contain real-world vulnerabilities and their fixes for detection and repair research.

# Software Vulnerability Datasets: Sorted by Most Recent Updates

Based on the comprehensive dataset analysis from our previous conversation, here is the complete list of **16 software vulnerability datasets** sorted by their most recent updates, from newest to oldest:

![Comprehensive table of software vulnerability datasets sorted by most recent updates](https://ppl-ai-code-interpreter-files.s3.amazonaws.com/web/direct-files/e2c83492c1e1bcd042053fd2fe250f23/e97c37fa-3fe7-46a5-997e-8d3d68c0e7b4/beb55162.png)

Comprehensive table of software vulnerability datasets sorted by most recent updates

## Key Insights from the Sorted Analysis

### **Most Current Datasets (2024-2025)**

**ICVul (2025)** stands as the newest dataset, representing the latest advancement in vulnerability research with enhanced metadata including Vulnerability-Contributing Commits (VCCs) and improved labeling reliability.

**CVEfixes (2024)** maintains its position as the most actively updated dataset, with the latest version (v1.0.8) covering vulnerabilities up to July 2024. This continuous update cycle makes it highly valuable for current research.

**MoreFixes (2024)** offers the largest scale with **26,617 unique CVEs**, making it the most comprehensive dataset available for extensive vulnerability research.

**VulnPatchPairs (2024)** and **MegaVul (2024)** provide specialized approaches - paired vulnerability analysis and comprehensive C/C++ coverage respectively.

### **Established Recent Datasets (2021-2023)**

**DiverseVul (2023)** provides the most diverse project coverage with **18,945 vulnerable functions** across **295 new projects** not found in previous datasets.

The **2021 generation** includes PatchDB, CrossVul, and D2A, each offering unique methodological approaches - security-focused patching, multi-language coverage (40+ languages), and differential analysis respectively.

### **Classic Benchmarks (2018-2020)**

**BigVul (2020)**, **Devign (2019)**, and **VulDeePecker (2018)** remain essential benchmarks in vulnerability detection research, despite their age. These datasets continue to be widely cited and used for baseline comparisons.

**SySeVR (2018)** contains the largest number of vulnerability candidates with **420,627 SeVCs**, though its semantic-based approach requires careful consideration for modern applications.

### **Continuously Updated Standards**

**SARD/Juliet** represents a special category with continuous updates from NIST, maintaining **450,000+ test cases** covering **150+ CWE classes**. While including synthetic cases, it provides the most comprehensive coverage of vulnerability types.


## Key Considerations for Dataset Selection

**For Comprehensive Research:** MoreFixes or CVEfixes provide the largest scale and best coverage.

**For C/C++ Specific Work:** MegaVul or DiverseVul offer the most comprehensive C/C++ vulnerability collections.

**For Multi-Language Studies:** CrossVul supports 40+ programming languages.

**For High-Quality Labels:** DiverseVul and ICVul emphasize label accuracy and quality control.

**For Patch Analysis:** VulnPatchPairs and D2A specifically focus on before/after fix comparisons.

**For Established Baselines:** Devign, BigVul, and VulDeePecker remain standard benchmarks in vulnerability detection literature.

**For cutting-edge research:** Use ICVul (2025) or CVEfixes (2024) for the most current vulnerabilities and methodologies.

**For large-scale studies:** MoreFixes (2024) provides the largest comprehensive dataset.

**For comparative studies:** Include classic benchmarks (BigVul, Devign) alongside recent datasets for baseline comparisons.

**For specialized applications:** Choose based on language requirements (MegaVul for C/C++, CrossVul for multi-language) or specific research focus (SecurityEval for code generation, PatchDB for security patches).

These datasets collectively represent the most comprehensive collection of realistic software vulnerabilities with their fixes, enabling advanced research in vulnerability detection, automated program repair, and security analysis across multiple programming languages and vulnerability types.

