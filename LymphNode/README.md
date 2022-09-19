
This task have completed using rules and RegEx. 

# rules 

## This rules used in Roman Removal:
| Attempt | Type |
| :---: | :---: |
| Type3 | 'I', 'II','III', 'IV', 'V', 'VI', 'VII', 'VIII','IX', 'X' | 
| Type4 | 'a', 'b','c', 'd', 'e', 'f', 'g', 'h','i', 'j' | 

## Rules
1. Remove Sentence Starting Digits : `remove_digit`
- remove `{digits}{.}|{digits}{)}`
- replace `.` with `{nothing}`
- remove extra spaces
- See below example:
```
input = '1. LEVEL III LYMPHNODES: 09 LYMPHNODES ISOLATED'
output = 'LEVEL III LYMPHNODES: 09 LYMPHNODES ISOLATED'
```

2. Remove Sentence Starting Roman : `remove_roman`
- Built RegEx patterns uing above types as `regex`
- Take first 5 characters -> then remove `{roman}{.}`
- Take first 5 characters -> replace `(` with `{nothing}` -> then remove `{roman}{)}` - > return output of first 5 characters + rest text
- replace `.` with `{nothing}`
```
input = 'IV. LEVEL III LYMPHNODES: 09 LYMPHNODES ISOLATED'
output = 'LEVEL III LYMPHNODES: 09 LYMPHNODES ISOLATED'
```

3. Get lymph node level / extract preceding word
- pass remove_digit and remove_roman output to this function
- split text by `: or ; or -`
- Remove extra spaces and get preceding words
```
input = 'LEVEL III LYMPHNODES: 09 LYMPHNODES ISOLATED'
output = 'LEVEL III LYMPHNODES'
```

4. Get positive and Isolated values Ex. (2/15)
- iterate entire note/text using `\n` (iterated for every single row)
- search isolated and positive pattern in every line of text
- isolated_positive:
```
input = 'LEVEL III LYMPHNODES: (2/15) LYMPHNODES ISOLATED'
output = '2,15'
```
5. Finally get lymph_prev_word, positive and Isolated values
- apply above functions on dataframe and get 3 columns in output dataframe
- column names: `positive`	`isolated`	`lymph_prev_word`

6. Apply function on a dataframe
- At end output file we will return following columns
- column names: `name`  |  `positive` | 	`isolated` | 	`lymph_prev_word`
- Note: name is the name of report ex. `MANGO_LYMPHNODE_REPORT_1`

In final output data one entry/report might have multiple outputs. we have stored data using name column to understand the multiple outputs.

