# mmseg

MMSEG is a word identification program for Chinese text based (mainly) on two
variants of the maximum matching algorithm. These algorithms are discussed
in MMSEG.TXT. By Chih-Hao Tsai. Email: c-tsai4@uiuc.edu. Last modified 3/6/98.

Usage: MMSEG file1 file2 path [complexity] [report level]

file1           Source file to be processed
file2           Target file to write segmented text to
path            Where the lexicon can be found
complexity      (Optional) Complexity of matching algorithm:
       simple   Simple (1 word) matching (default)
      complex   Complex (3-word chunk) matching
report level    (Optional) (For complex matching only): Progress report sent
                to standard output (screen) during segmentation:
      verbose   Display (1) All ambiguous segmentations and the length,
                variance of word lengths, average word length, and sum of
                log(frequency) for each each segmentation (2) Number of
                ambiguous segmentations not resolved by each disambiguation
                rule, and at which rule the ambiguity is resolved
     standard   Display (2) only
        quiet   None of the above information will be displayed

Example: mmseg in.txt out.txt ./lexicon/ complex quiet

## compile
```
scripts/compile.sh
```