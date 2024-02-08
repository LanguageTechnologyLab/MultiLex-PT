
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
    <td>Id number that is made up of the original instance id (e.g. 01) from pre-existing dataset and a new id (e.g. 104): 01-104</td>
  </tr>
    
  <tr>
    <td><b>genre</b></td>
    <td>Genre the extract was taken from.</td>
  </tr>
    
  <tr>
    <td><b>pt_word</b></td>
    <td>The target word.</td>
  </tr>
    
  <tr>
    <td><b>recapitalized_sent</b></td>
    <td>The context of the target word.</td>
  </tr>
    
  <tr>
    <td><b>pt_sentence_bold</b></td>
    <td>The context of the target word with the target word in bold as presented to annotators.</td>
  </tr>
    
  <tr>
    <td><b>num_annotators</b></td>
    <td>Number of annotators that annotated the instance.</td>
  </tr>

  <tr>
    <td><b>min_annotation_time</b></td>
  <td>The least amount of time taken to annotate the instance.</td>
  </tr>

<tr>
    <td><b>max_annotation_time</b></td>
  <td>The longest amount of time taken to annotate the instance.</td>
  </tr>

 <tr>
    <td><b>avg_annotation_time</b></td>
  <td>Average time spent annotating the instance.</td>
  </tr>

 <tr>
    <td><b>num_candidate_substitutions</b></td>
  <td>Total number of suggested simplifications. </td>
  </tr>

 <tr>
    <td><b>num_unqiue_candidate_substituions</b></td>
  <td>Number of unique simplifications suggested.</td>
  </tr>

 <tr>
    <td><b>gold_complexity_value</b></td>
  <td>Averaged returned complexity assigned by the annotators. <b>Currently unavailable due to MLSP-2024 (see below)</b. </td>
  </tr>

  <tr>
    <td><b>gold_candidate_substitutions</b></td>
  <td>Suggested simplifications ranked per suggestion frequency. <b>Currently unavailable due to MLSP-2024 (see below)</b. </td>
  </tr>
     
     

</table>

## Use in Python

You can load the dataset into your prefered IDE via the following code.

```
import pandas as pd

pd.read_csv("MultiLex.tsv", sep="\t", encoding="utf-8")
```

 Please see the following link for a full tutorial on how to use Pandas: https://pandas.pydata.org/docs/user_guide/index.html#user-guide.


## Full Release TBC
Full release of the dataset, including gold labels, shall be made available after the completion of the Multilingual Lexical Simplification Pipeline (MLSP-2024) shared-task hosted at BEA. This shared-task uses data from MultiLex-PT meaning that full release of the dataset would result in an unfair advantage.

For more information on MLSP-2024 please see: https://sites.google.com/view/mlsp-sharedtask-2024/home

## License

CC0 1.0 Universal


