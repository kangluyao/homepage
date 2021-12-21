---
title: How to submit sequence data to NCBI
date: '2021-06-29'
slug: submit sequence data to NCBI
---

First, download the **aspera** from the NCBI to the local directory, locate to this directory and run `cmd`. Then use the Aspera command line for the SRA Submission.

```
ascp -i E:\to_NCBI\aspera.openssh -QT -l100m -k1 -d E:\micro1\its\amplicon\temp subasp@upload.ncbi.nlm.nih.gov:uploads/lykang_ibcas.ac.cn_zKuNmDGA
```
#`E:\micro1\its\amplicon\temp` is the directory where the fastq files are stored
#`Lykang_ibcas.ac.cn_zKuNmDGA` is the directory given by NCBI when upload data. I need to upload my sequence data to this folder from my local server.

