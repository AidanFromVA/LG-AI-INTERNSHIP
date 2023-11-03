#DatasetInfo.
## train.csv [File] 598(rows) * 2881(columns)
PRODUCT_ID: Unique ID of the product
Y_Class: Product quality status (Target) (0: below standard, 1: suitable, 2: exceeding standard)
Y_Quality: Product quality value
TIMESTAMP: Time when the product entered the process
LINE: Type of process LINE the product entered ('T050304', 'T050307', 'T100304', 'T100306', 'T010306', 'T010305' exist)
PRODUCT_CODE: Product CODE number ('A_31', 'T_31', 'O_31' exists)
X_1 ~ X_2875: Variables extracted during the process and de-identified

## test.csv [file]
PRODUCT_ID: Unique ID of the product
TIMESTAMP: Time when the product entered the process
LINE: Type of process LINE the product entered ('T050304', 'T050307', 'T100304', 'T100306', 'T010306', 'T010305' exist)
PRODUCT_CODE: Product CODE number ('A_31', 'T_31', 'O_31' exists)
X_1 ~ X_2875: Variables extracted during the process and de-identified

## sample_submission.csv [file] - submission form
PRODUCT_ID: Unique ID of the product
Y_Class: Predicted product quality status (0: below standard, 1: suitable, 2: exceeding standard)
