
# HyDe Input Preparation Script

This is a script to prepare VCF data for hybridization analysis using HyDe.

---

## About

This repository provides a script to convert a multi-sample VCF file into a PHYLIP-format alignment suitable for HyDe.
It handles:
- Selecting specific individuals
- Generating two pseudo-haploid sequences per individual (`a` and `b`)
- Strict PHYLIP formatting (10-character names, no missing SNPs)

---

## Files

- `hyde_inputs.py`:
  Main script to parse VCF and generate PHYLIP and MAP files for HyDe.

---

## Usage

1. **Prepare a sample list file** (tab-separated):

```
10042  pop1
8389   pop1
10219  pop2
8388   pop2
...
```

2. **Run the script**:

```bash
python hyde_inputs.py -v your_data.vcf -k indivs_list.txt -o hyde_input.phy -m map_file.txt
```

Arguments:
- `-v` : input VCF file (plain text, uncompressed)
- `-k` : file with individuals to keep (tab-separated: sample and population name)
- `-o` : output PHYLIP file
- `-m` : output MAP file

---

## Requirements

- Python 3.x
- Works directly with plain (unzipped) VCF files.

---

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## Citation

If you use these scripts in your project, please cite the original HyDe paper:

Blischak, P.D., Chifman, J., Wolfe, A.D., and Kubatko, L.S. (2018).
HyDe: A Python package for genome-scale hybridization detection. *Systematic Biology*, 67(5), 821–829.

---
