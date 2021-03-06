## Deep learning enables therapeutic antibody optimization in mammalian cells by deciphering high-dimensional protein sequence space.

### Abstract

Therapeutic antibody optimization is time and resource intensive, largely because it requires low-throughput screening (103 variants) of full-length IgG in mammalian cells, typically resulting in only a few optimized leads. Here, we use deep learning to interrogate and predict antigen-specificity from a massively diverse sequence space to identify globally optimized antibody variants. Using a mammalian display platform and the therapeutic antibody trastuzumab, rationally designed site-directed mutagenesis libraries are introduced by CRISPR/Cas9-mediated homology-directed repair (HDR). Screening and deep sequencing of relatively small libraries (104) produced high quality data capable of training deep neural networks that accurately predict antigen-binding based on antibody sequence. Deep learning is then used to predict millions of antigen binders from an in silico library of ~108 variants, where experimental testing of 30 randomly selected variants showed all 30 retained antigen specificity. The full set of in silico predicted binders is then subjected to multiple developability filters, resulting in thousands of highly-optimized lead candidates. With its scalability and capacity to interrogate  high-dimensional protein sequence space, deep learning offers great potential for antibody engineering and optimization.

### Model structure

![avatar](LSTM_model_struct.png)

![avatar](CNN_model_struct.png)

| Model name | Input | Output | Loss Function | Model structure |
| ---------- | ----- | ------ | ------------- | --------------- |
| LSTM RNN classifier | Amino acid sequence of length 10 (CDRH3 only) without gap | Probability of binding | Binary cross entropy | LSTM-RNN (3 layers, 40 hidden nodes, dropout rate = 0.1) + sigmoid activation |  
| CNN classifier | Amino acid sequence of length 10 (CDRH3 only) without gap | Probability of binding | Binary cross entropy | CNN (400 filters, kernel size 3, stride 1) + max pooling + FC + Relu activateion | 

### Reference

Mason et al. [https://www.biorxiv.org/content/10.1101/617860v3]

	
