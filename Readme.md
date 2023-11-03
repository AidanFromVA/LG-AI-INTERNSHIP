# Development of a product quality classification AI model to build a smart factory control system

## Preliminaries
   - '23.01.01 ~ '23.02.28
<hr>

Try1: feature selection
- Forward selection method, backward elimination method
- Remove VIF criteria
- Recursive Feature Elimination (RFE)

Try2: Handling missing value
- Apply mean, median, mode, and iterative imputer techniques for each factory
- Apply mean, median, mode, and iterative imputer techniques for each product

Try3: attempt semi-supervised learning
- Add Y_Quality column to test dataset -> Y_Class prediction

Try4: Data Augmentation
- Use CTGAN

Try5: tablur dataset -> Graph dataset construction
- GNN (GCN applied)

Try6: Modeling comparison
- Linear, Lasso, Ridge, Elastic net
- GBM, LGBM, Catboost
- DT, RF
-GCN

solution:
   - Feature selection: Best not to do it according to public score
   - Handling missing value: Replace missing values with -1
   - Y_Quality log transformation applied
   - Establish multi model for each PRODCUT
   - Modification of decision boundary according to evaluation method Macro F1 score

### Final Try:
Curse of dimensionality expected due to feature increase (2875 -> 3326)
     - feature elimination based on corr
     - Integrated into one feature through PCA over corr threshold (0.9).
    
### Final Solution: Building a multi model and dynamically adjusting the decision boundary using a decision tree
   - Preliminary data model 1
   - Main line data model 2
   - Full data model 3
