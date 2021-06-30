# Cicer reticulatum annotation
Structural and functional annotation of Cicer reticulatum´s chromosome 4  
  
  This is an initial version described in:  
Carmona, Alejandro (2020/2021) Anotación estructural y funcional del cromosoma 4 de Cicer reticulatum. Final Master Thesis. University of Cordoba.  

The annotation for the current version contains the following files:  
  
  * Mapped - GFF  
  * Unmapped - TXT, list of unmapped  
  
This is the description of the code used in the following tools:  
  
  * Helitron  
          
        java -jar HelitronScanner.jar scanHead -lf ../TrainingSet/head.lcvs -g FASTA -bs 0 -o FILE  
        java -jar HelitronScanner.jar scanTail -lf ../TrainingSet/tail.lcvs -g FASTA -bs 0 -o FILE  
        java -jar HelitronScanner.jar pairends -hs head FILE -ts tail FILE -o FILE  
        java -jar HelitronScanner.jar draw -p paired File -g FASTA -o FILE --pure
      
  * Liftoff  

        liftoff  -g GFF -o FILE -u FILE -m PATH -copies target reference
