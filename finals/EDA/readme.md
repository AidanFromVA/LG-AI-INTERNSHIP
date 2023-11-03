Compared to the preliminaries, data was added (row increased) and features increased (2875 -> 3326).

## Dataset Info.

## train.csv [file]
PRODUCT_ID: Unique ID of the product.
Y_Class: Product quality status (Target)
0: Failure to meet appropriate standards (unsuitable).
1: Suitable.
2: Exceeding the appropriate standard (non-conformance).
Y_Quality: Quantitative figures related to product quality.
LINE: Type of process LINE the product entered ('T050304', 'T050307', 'T100304', 'T100306', 'T010306', 'T010305' exist).
PRODUCT_CODE: Product CODE number ('A_31', 'T_31', 'O_31' exists).
X_1 ~ X_3326: Variables extracted during the process and de-identified.


## test.csv [file].
PRODUCT_ID: Unique ID of the product
LINE: Type of process LINE the product entered ('T050304', 'T050307', 'T100304', 'T100306', 'T010306', 'T010305' exist).
PRODUCT_CODE: Product CODE number ('A_31', 'T_31', 'O_31' exists).
X_1 ~ X_3326: Variables extracted during the process and de-identified.


## sample_submission.csv [file] - submission form
PRODUCT_ID: Unique ID of the product.
Y_Class: Predicted product quality status.
0: Failure to meet appropriate standards (unsuitable).
1: Suitable.
2: Exceeding the appropriate standard (non-conformance).

This is data from the actual process, and some variables have been de-identified for security reasons. (X variable).
'LINE' and 'PRODUCT_CODE' are of the same type for both Train and Test.
