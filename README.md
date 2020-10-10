# Kaggle-OpenVaccine
 Kaggle competition "OpenVaccine: COVID-19 mRNA Vaccine Degradation Prediction"
 
 This is my solution (top 19%) to the Kaggle competition "OpenVaccine: COVID-19 mRNA Vaccine Degradation Prediction"
 https://www.kaggle.com/c/stanford-covid-vaccine
 
 ## Data
 - Attributes: RNA sequence and structure at each position
  - RNA sequence
  - RNA structure
  - RNA predicted loop type
  - RNA pairing probability matrix (BPPS)
 - Target: Degradabilities under five conditions at each position
 
 ## Metrics
 - Columnwise averaged RMSE
 
 ## Models
 - RNN-based sequence model
 - Multi-layer bi-directional GRU/LSTM layers
 - Embedding layers to translate RNA sequence and structure (14 tokens) into dense features
 - Additional BPPS and RNA-based features
 - Model blending from different cross validation training sets
 
 ## Training
 - Weighted training using the signal-to-noise ratio as sample weight
 - 50-100 epochs
 - 4-fold cross validation
 
 ## Results
 - Public leaderboard: 0.2393 (ranked 312/1636, top 19%)
 - Private leaderboard: 0.3556 (ranked 300/1636, top 19%)
 
 ## Ideas tried but not worked
 - Add Conv1d layer with batch/layer normalization
 - Use k-mer to encode RNA
