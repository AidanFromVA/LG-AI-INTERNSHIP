## [LG Aimers Smart Factory Product Quality Status Classification AI]

# 1. EDA progress
#2.Try
   - Try1: feature selection
     - Forward selection method
     - Backwards elimination method
     - Remove VIF criteria
     - Recursive Feature Elimination (RFE)
   - Try2: Handling missing value
     - Apply mean, median, mode, and iterative imputer techniques for each factory
     - Apply mean, median, mode, and iterative imputer techniques for each product
   - Try3: attempt semi-supervised learning
     - Add Y_Quality column to test dataset -> Y_Class prediction
   - Try4: Data Augmentation
     - Use CTGAN
   - Try5: tablur dataset -> Graph dataset construction
     - GNN (GCN applied)
   - Try6: Modeling comparison
     - Linear, Lasso, Ridge, Elastic net
     - GBM, LGBM, Catboost
     - DT, RF
     -GCN

#3.solution
   - Feature selection: Best not to do it according to public score
   - Handling missing value: Replace missing values with -1
   - Y_Quality log transformation applied
   - Establish multi model for each PRODCUT
   - Modification of decision boundary according to evaluation method Macro F1 score
