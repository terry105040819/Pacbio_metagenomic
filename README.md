### Pacbio_pathogenic_detection_pipeline
首先先從Pacbio smrt links抓取下機檔案(.fastq.gz)

參考Pacbio官方的github進行安裝`https://github.com/PacificBiosciences/pb-metagenomics-tools`
利用git clone將pb-metagenomic-tool提取到伺服器中

安裝相關的dependences

* HiFi-MAG-Pipeline
  運行pipeline前須先將HiFi reads進行Assemble，官方推薦metaFlye和hifiasm進行組裝

  Flye
  ```shell
  flye --pacbio-hifi ~/input.fastq --meta --out-dir ~/output-dir
  ```



* Taxonomy-Profiling-Sourmash(Assembly free)
