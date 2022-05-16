## Text Extraction Using Regular Expression In Python

#### Requirements: 
Run on Jupyter Notebook/Colab. Chnage the document path extension accordingly

#### Procedure:

#### 1. Using PDF Miner library I converted all the data from the pdf to textual data in the form of string. We can use this string data to query the CPT codes from it

#### 2. Do some data cleaning, first replacing the "*" in the data with space so that we can easily get CPT codes which have asterick in it. Also we need to remove the footers that are in each page. Since the footer consist of the number 2020. We don't want our code to consider it as a CPT code

#### 3. Using regular expressions to generate a particular CPT code. After analyzing the document, I found that there are many CPT codes of different variation. And few of them are not even numeric.

#### I am generating three columns in my dataframe.
1. All the numeric CPT codes which requires prior authorization
2. All the non-numeric which is the combination of the codes which requires prior authorization
3. All the codes which do not require prior authorization
4. And finally all the CPT codes in the document

#### 4. Save the file as csv.

#### 5. Observation: Based on my observation few codes in the breast reconstruction does not require a prior authorization. Hence I decided to have a separate column for it. There might be multiple ways in which we can have more filtered results, like based on the procedure name e.g Arthoplasty we only generate the CPT codes for that procedure only, that can also be done, studying the location in it and also deciding a terminating index can work to get such customised CPT codes.
