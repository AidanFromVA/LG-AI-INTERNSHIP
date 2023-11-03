# Development of a product quality classification AI model to build a smart factory control system
![image](https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/5e3fa0a0-456f-4300-8d4e-147e48ea6f90)

## Preliminaries
   - '23.01.01 ~ '23.02.28
## Summary
<img width="1090" alt="Screenshot 2023-11-03 at 5 57 54 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/0505e130-f9b8-4bd9-b6b2-77e314107083">

## Outline
<img width="1083" alt="Screenshot 2023-11-03 at 5 59 03 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/496eeda0-3b3b-44f7-981a-01704d744358">

## Data
<img width="1082" alt="Screenshot 2023-11-03 at 5 59 14 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/31a4e0ee-0c7d-4c11-b089-b22a9e593075">

<img width="1082" alt="Screenshot 2023-11-03 at 5 59 14 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/54acceee-53e5-47d4-a2e2-fdccc62b4d1b">

<img width="1084" alt="Screenshot 2023-11-03 at 6 01 24 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/437d818e-a7bf-42de-8b4b-e4547fa2c87b">

<img width="1079" alt="Screenshot 2023-11-03 at 6 01 30 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/d424291a-2f9e-41a2-bbbb-16cf80dc1193">

<img width="1082" alt="Screenshot 2023-11-03 at 6 01 36 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/88688b0a-57d1-463a-b498-71e62782be20">

## Solution
<img width="1087" alt="Screenshot 2023-11-03 at 6 03 24 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/2cad6986-fd74-429b-9cc3-aae29da36fce">

<img width="1086" alt="Screenshot 2023-11-03 at 6 03 30 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/4e59879e-4a6b-4c74-abe1-ab75de4b3810">

<img width="1080" alt="Screenshot 2023-11-03 at 6 03 38 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/841d1e77-4ecf-4230-9d87-04411daeee21">

<img width="1087" alt="Screenshot 2023-11-03 at 6 03 46 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/32f89c3b-920f-45db-8b7e-9453669d6383">

<img width="1083" alt="Screenshot 2023-11-03 at 6 03 53 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/49bfba1d-f0be-46b2-a6a7-b35a1ebe6ae1">

<img width="1086" alt="Screenshot 2023-11-03 at 6 04 57 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/9b60d05c-7514-4923-a0af-f79ad8a2da77">

<img width="1080" alt="Screenshot 2023-11-03 at 6 05 03 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/b4f597a3-4387-485c-b82d-ec7ab3d9527e">

<img width="1086" alt="Screenshot 2023-11-03 at 6 05 08 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/8add44e1-02f0-41ed-99e4-ca3f5a35e2fe">

## Solution

<img width="1089" alt="Screenshot 2023-11-03 at 6 06 00 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/2f8f4ede-d2a5-40d1-8453-08d183879fd1">

<img width="1085" alt="Screenshot 2023-11-03 at 6 06 14 PM" src="https://github.com/byungkwon2023F/LG-AI-INTERNSHIP/assets/88296556/004c8fe7-589d-4c53-99a3-3a9bc5b445eb">

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

