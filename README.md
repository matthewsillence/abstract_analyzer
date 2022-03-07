# abstract_analyzer
Python scripts to analyze the composition of academic abstracts for doctoral thesis using NLTK.

## Obtaining the thesis metadata
The metadata for for the abstract analyzer can be downloaded from https://ueaeprints.uea.ac.uk/. Use the Advanced Search option to select the Faculty or School of Study and the Item Type ('thesis').

When the search results are displayed, you will be given the option to export the results. From the drop-down box, select 'Multiline CSV' and click 'Export'.

Save the file locally, or upload to the Google Colaboratory directory.

## Data Preparation
The first part of the Python script used Pandas to read in the repository CSV file and idolate the column with the thesis abstract data. This content is then written to an 'abstracts.csv.' The CSV data is then rewritten as the text file 'abstracts.txt'.

## Text Tokenization
The text is tokenized using NLTK, and punctuation is removed. The total number of tokens in the text file can be displayed.

## Reading Text Lines
Each line in the text file needs to be read and tokenized using a loop. A conditional statement of lines with missing data (where rows in the original CSV file had no abstract) are filtered out. The number of sentences and words per abstract can be displayed, and the average number of words per sentence calculated.

## Parts of Speech Tagging
Using the parts of speech tagger from NLTK, and reading and tokenizing each sentence and word in each line, this loop returns a list containing the tokens and their equivalent tag.

## Exporting the Tokens and Tags
The final part of the script creates a dataframe of the tags using Pandas, which is saved to the CSV file 'tags.csv'.
