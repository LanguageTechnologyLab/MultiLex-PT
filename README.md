
# MultiLex-PT
MultiLex-PT is the first Portuguese Lexical Simplification (LS) dataset constructed using the MultiLex framework to cater for all tasks within the LS pipeline, ranging from lexical complexity prediction to substitute generation, selection, and ranking.

MultiLex-PT contains 5,165 instances from the Bible (2,321), news articles (1,817), and biomedical texts (1,0237) and provides continuous complexity values alongside gold candidate simplifications. 

Bible instances were obtained from Portuguese translations of the King James Bible. News instances were scraped from the PorSimplesSent dataset [(Leal, et al., 2018)](https://aclanthology.org/C18-1034/) as well as from the [CC-News (Common Crawl-News) corpus](https://commoncrawl.org/blog/news-dataset-available). Biomedical instances were extracted from abstracts of biomedical literature supplied by WMT-2019 [(Bawden, et al., 2019)](https://aclanthology.org/W19-5403/).


## Dataset Format
<table>
    
   <tr>
    <th>Header</th>
    <th>Description</th>
  </tr>
 
    
  <tr>
    <td><b>ID</b></td>
    <td>Instance id that is made up of the original instance id (e.g. 01) and the new additional context id. (e.g. 104): 01-104.</td>
  </tr>
    
   <tr>
    <td><b>ALEXSIS.CW</b></td>
    <td>The original complex word taken form ALEXSIS and used at TSAR-2022.</td>
  </tr>
    
  <tr>
    <td><b>ALEXSIS.Context</b></td>
    <td>The original context for the given complex word taken form ALEXSIS and used at TSAR-2022.</td>
  </tr>
    
  <tr>
    <td><b>Candidate.Subs@n</b></td>
    <td>The candidate substitutions generated using MLM on the instances provided by TSAR-2022.</td>
  </tr>
    
  <tr>
    <td><b>Additional.Context</b></td>
    <td>New additional context obtained from the CC-News dataset.</td>
  </tr>
    
  <tr>
    <td><b>Additional.Subs@n</b></td>
    <td>New additional candidate substitutions generated using MLM on the additional contexts taken from the CC-News dataset</td>
  </tr>
    
  <tr>
    <td><b>Sent.Sim</b></td>
    <td>The cosine similarities between the SBert sentence embedding of the additional context and the original context provided by TSAR-2022.</td>
  </tr>

  <tr>
    <td><b>Word.Sim@n</b></td>
  <td>The cosine similarities between the word embeddings of the additional candidate substitutions and the original complex word provided by TSAR-2022.</td>
  </tr>
     
  <tr>
    <td><b>Gold.Label@n</b></td>
    <td>The original gold candidate substitutions provided by TSAR-2022.</td>
  </tr>    

</table>

## Use in Python
```
import pandas as pd

pd.read_csv("MultiLex.tsv", sep="\t", encoding="utf-8")

```


## Full Release TBC
Full release of the dataset, including gold labels, shall be made available after the completion of the Multilingual Lexical Simplification Pipeline (MLSP-2024) shared-task hosted at BEA. 

For more information on MLSP-2024 please see: https://sites.google.com/view/mlsp-sharedtask-2024/home

## License



