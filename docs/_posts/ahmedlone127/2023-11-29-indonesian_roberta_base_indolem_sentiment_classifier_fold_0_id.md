---
layout: model
title: Indonesian indonesian_roberta_base_indolem_sentiment_classifier_fold_0 RoBertaForSequenceClassification from w11wo
author: John Snow Labs
name: indonesian_roberta_base_indolem_sentiment_classifier_fold_0
date: 2023-11-29
tags: [roberta, id, open_source, sequence_classification, onnx]
task: Text Classification
language: id
edition: Spark NLP 5.2.0
spark_version: 3.0
supported: true
engine: onnx
annotator: RoBertaForSequenceClassification
article_header:
  type: cover
use_language_switcher: "Python-Scala-Java"
---

## Description

Pretrained RoBertaForSequenceClassification model, adapted from Hugging Face and curated to provide scalability and production-readiness using Spark NLP.`indonesian_roberta_base_indolem_sentiment_classifier_fold_0` is a Indonesian model originally trained by w11wo.

{:.btn-box}
<button class="button button-orange" disabled>Live Demo</button>
<button class="button button-orange" disabled>Open in Colab</button>
[Download](https://s3.amazonaws.com/auxdata.johnsnowlabs.com/public/models/indonesian_roberta_base_indolem_sentiment_classifier_fold_0_id_5.2.0_3.0_1701278893799.zip){:.button.button-orange.button-orange-trans.arr.button-icon}
[Copy S3 URI](s3://auxdata.johnsnowlabs.com/public/models/indonesian_roberta_base_indolem_sentiment_classifier_fold_0_id_5.2.0_3.0_1701278893799.zip){:.button.button-orange.button-orange-trans.button-icon.button-copy-s3}

## How to use



<div class="tabs-box" markdown="1">
{% include programmingLanguageSelectScalaPythonNLU.html %}
```python

document_assembler = DocumentAssembler()\
    .setInputCol("text")\
    .setOutputCol("document")

tokenizer = Tokenizer()\
    .setInputCols("document")\
    .setOutputCol("token")  
    
sequenceClassifier = RoBertaForSequenceClassification.pretrained("indonesian_roberta_base_indolem_sentiment_classifier_fold_0","id")\
            .setInputCols(["document","token"])\
            .setOutputCol("class")

pipeline = Pipeline().setStages([document_assembler, tokenizer, sequenceClassifier])

data = spark.createDataFrame([["PUT YOUR STRING HERE"]]).toDF("text")

result = pipeline.fit(data).transform(data)

```
```scala

val document_assembler = new DocumentAssembler()
    .setInputCol("text")
    .setOutputCol("document")

val tokenizer = new Tokenizer()
    .setInputCols("document") 
    .setOutputCol("token")  
    
val sequenceClassifier = RoBertaForSequenceClassification.pretrained("indonesian_roberta_base_indolem_sentiment_classifier_fold_0","id")
            .setInputCols(Array("document","token"))
            .setOutputCol("class")

val pipeline = new Pipeline().setStages(Array(documentAssembler, tokenizer, sequenceClassifier))

val data = Seq("PUT YOUR STRING HERE").toDS.toDF("text")

val result = pipeline.fit(data).transform(data)


```
</div>

{:.model-param}
## Model Information

{:.table-model}
|---|---|
|Model Name:|indonesian_roberta_base_indolem_sentiment_classifier_fold_0|
|Compatibility:|Spark NLP 5.2.0+|
|License:|Open Source|
|Edition:|Official|
|Input Labels:|[documents, token]|
|Output Labels:|[class]|
|Language:|id|
|Size:|467.6 MB|

## References

https://huggingface.co/w11wo/indonesian-roberta-base-indolem-sentiment-classifier-fold-0