### Pacbio_pathogenic_detection_pipeline
首先先從Pacbio smart links抓取下機檔案(.fastq.gz)

參考Pacbio官方的github進行安裝`https://github.com/PacificBiosciences/pb-metagenomics-tools`

以Python3.12.5建立環境(這邊使用Mamba解決Conda solving environment過久的問題)
```shell
 mamba create -n pacbio_new312 python=3.12.5
```
