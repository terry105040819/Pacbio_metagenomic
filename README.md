### Pacbio_pathogenic_detection_pipeline
---
首先先從Pacbio smrt links抓取下機檔案(.fastq.gz)

>參考Pacbio官方的github進行安裝`https://github.com/PacificBiosciences/pb-metagenomics-tools`
>>git clone將pb-metagenomic-tool提取到伺服器中
>>>利用Pb_metagenomic_tools資料夾中的snakemake-environment.yaml將環境所需dependences複製到主機中
>>>>conda env create -f snakemake-environment.yml

主要使用分析流程分為需Assemble的HiFi-MAG-pipeline與Assemble-free的Taxonomic-Sourmash-pipeline,可以根據研究目的擇一運行

![image](https://github.com/user-attachments/assets/3cce7635-eae6-4444-8b9c-0887daef63f8)



* HiFi-MAG-Pipeline
  運行pipeline前須先將HiFi reads進行Assemble，官方推薦metaFlye和hifiasm進行組裝


  Flye
  ```shell
  flye --pacbio-hifi ~/input.fastq --meta --out-dir ~/output-dir
  ``



* Taxonomy-Profiling-Sourmash(Assembly free)
