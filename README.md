# Telomere-to-Telomere diploid Indian Genome 
We have sequenced a EBV-immortalized human male cell line from SG10k samples on different platforms. The data contains ~106x of Pacbio HiFi, ~64x of Oxford Nanopore (ONT) Duplex, ~222x ONT Ultralong (ULONT), ~100x MGI WGS short reads, ~33x Illumina WGS short reads and ~120x Omni-C for the child sample (I002C). Statistics of BioNano will be added soon.

For parental samples:
SampleType | SampleID | HiFi (REVIO) | Duplex | MGI
---|:---:|:---:|:---:|:---:|
Father|I002A|60x|21x|35x
Mother|I002B|61x|20x|37x

The data statistics are provided in an [excel](Data/Reads)

# Assembly release

### v0.7
The latest version of assembly with combined QV of 82.
- Maternal [Fasta](https://figshare.com/ndownloader/files/53198075)
- Paternal [Fasta](https://figshare.com/ndownloader/files/53238263) 

Reads can be downloaded from SRA [PRJNA1150503](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1150503). Please cite the below article if you use the dataset.

Sarashetti, P., Lipovac, J., Tomas, F. et al. Evaluating data requirements for high-quality haplotype-resolved genomes for creating robust pangenome references. Genome Biol 25, 312 (2024). https://doi.org/10.1186/s13059-024-03452-y
### v0.4

This assembly version results from performing two rounds of polishing, as outlined in the procedure from [^1].
- Maternal: [Fasta](https://figshare.com/ndownloader/files/46211781?private_link=56295c4b2905cef7187f) 
- Paternal: [Fasta](https://figshare.com/ndownloader/files/46211697?private_link=c8a5045cd96979c86939) 

The v0.4 assembly has a improved QV values, with Maternal at 72.35 and Paternal at 70.97. QV values are estimated using hybrid k-mers generated from Pacbio HiFi and MGI WGS data as described in [^2]. Chromosome wise QV values are listed in an [excel](Data/Assembly) file. 

### v0.2

This version of the assembly contains Telomere-to-Telomere chromsomes for both maternal and paternal haplotypes including a mitochondria. In this version of the genomes, rDNAs have not been resolved. 

 &nbsp;|Maternal|Paternal
---|:---:|:---:
T2T Chromosomes|23|23
Size|3,022,465,370|2,934,829,127
NG50|154,891,367|146,273,588
%GC|40.82|40.79

Assembly files (zipped): 
- Maternal: [Fasta](https://figshare.com/ndownloader/files/44506250) 
- Paternal: [Fasta](https://figshare.com/ndownloader/files/44506241) 
- Mitochondira: [Fasta](https://figshare.com/ndownloader/files/44506232) 

If you wish to download the files using wget, you may use `wget -O <haplotype>.fasta.gz <link>`

Assembly QV is calculated with [yak](https://github.com/lh3/yak) tool using I002C MGI WGS dataset. Per chromosome QV values are provided in an [excel](Data/Assembly) file

**Note:** The data available on this GitHub page can be accessed either from [LHG](https://github.com/LHG-GG/I002C) or [LBCB](https://github.com/lbcb-sci/I002C) GitHub pages

[^1]: Mc Cartney, Ann M., et al. "Chasing perfection: validation and polishing strategies for telomere-to-telomere genome assemblies." Nature methods 19.6 (2022): 687-695.
[^2]: https://github.com/arangrhie/T2T-Polish/tree/master/merqury
