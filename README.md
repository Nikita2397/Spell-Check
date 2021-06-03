# Spell-Check
Given an erroneous word, this method considers all the words in the standard dictionary that are at a fixed Levenshtein Distance (commonly known as edit distance) from the erroneous word. 

Here for a given word we find all the words in the standard dictionary that are a fixed edit distance away from the given query (erroneous) word. This method takes care of all the candidate words that are ≤ 2 edit distance away from the query word. Following are the steps taken to achieve the task:

1. A simple edit to a word such as deletion (remove one letter), a transposition (swap two adjacent letters), a replacement (change one letter to another) or an insertion (add a letter) is implemented in the edits1 function

2. I did again similar edit in the edits2 function and I compare the resultant words with the existing words in the dictionary
Here I have considered big.txt as my corpus which is an EBook of The Adventures of Sherlock Holmes by Sir Arthur Conan Doyle consisting 1.1M words (Norvig’s big.txt)

3. After successful generation of the possible candidates for the misspelled word, I need to rank them. After converting the words into vector form, cosine similarity is implemented to find the closest three candidates and are suggested to the user.

