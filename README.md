
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
    <td><b>num_annotation</b></td>
    <td>Id number assigned to each instance.</td>
  </tr>
    
   <tr>
    <td><b>genre_id</b></td>
    <td>Instance id that is made up of the original instance id (e.g. 01) from pre-existing dataset and a new id (e.g. 104): 01-104</td>
  </tr>
    
  <tr>
    <td><b>genre</b></td>
    <td>The original context for the given complex word taken form ALEXSIS and used at TSAR-2022.</td>
  </tr>
    
  <tr>
    <td><b>pt_word</b></td>
    <td>.</td>
  </tr>
    
  <tr>
    <td><b>recapitalized_sent</b></td>
    <td></td>
  </tr>
    
  <tr>
    <td><b>pt_sentence_bold</b></td>
    <td></td>
  </tr>
    
  <tr>
    <td><b>num_annotators</b></td>
    <td></td>
  </tr>

  <tr>
    <td><b>min_annotation_time</b></td>
  <td></td>
  </tr>

<tr>
    <td><b>max_annotation_time</b></td>
  <td></td>
  </tr>

 <tr>
    <td><b>avg_annotation_time</b></td>
  <td></td>
  </tr>

 <tr>
    <td><b>num_candidate_substitutions</b></td>
  <td></td>
  </tr>

 <tr>
    <td><b>num_unqiue_candidate_substituions</b></td>
  <td></td>
  </tr>

 <tr>
    <td><b>Gold Complexity Value</b></td>
  <td></td>
  </tr>

  <tr>
    <td><b>Gold Candidate Substitutions</b></td>
  <td></td>
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



