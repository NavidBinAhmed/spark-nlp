---
layout: model
title: Turkish distilbert_base_turkish_cased_qa_pipeline pipeline DistilBertForQuestionAnswering from incidelen
author: John Snow Labs
name: distilbert_base_turkish_cased_qa_pipeline
date: 2024-09-07
tags: [tr, open_source, pipeline, onnx]
task: Question Answering
language: tr
edition: Spark NLP 5.5.0
spark_version: 3.0
supported: true
annotator: PipelineModel
article_header:
  type: cover
use_language_switcher: "Python-Scala-Java"
---

## Description

Pretrained DistilBertForQuestionAnswering, adapted from Hugging Face and curated to provide scalability and production-readiness using Spark NLP.`distilbert_base_turkish_cased_qa_pipeline` is a Turkish model originally trained by incidelen.

{:.btn-box}
<button class="button button-orange" disabled>Live Demo</button>
<button class="button button-orange" disabled>Open in Colab</button>
[Download](https://s3.amazonaws.com/auxdata.johnsnowlabs.com/public/models/distilbert_base_turkish_cased_qa_pipeline_tr_5.5.0_3.0_1725722322578.zip){:.button.button-orange.button-orange-trans.arr.button-icon}
[Copy S3 URI](s3://auxdata.johnsnowlabs.com/public/models/distilbert_base_turkish_cased_qa_pipeline_tr_5.5.0_3.0_1725722322578.zip){:.button.button-orange.button-orange-trans.button-icon.button-copy-s3}

## How to use



<div class="tabs-box" markdown="1">
{% include programmingLanguageSelectScalaPythonNLU.html %}
```python

pipeline = PretrainedPipeline("distilbert_base_turkish_cased_qa_pipeline", lang = "tr")
annotations =  pipeline.transform(df)   

```
```scala

val pipeline = new PretrainedPipeline("distilbert_base_turkish_cased_qa_pipeline", lang = "tr")
val annotations = pipeline.transform(df)

```
</div>

{:.model-param}
## Model Information

{:.table-model}
|---|---|
|Model Name:|distilbert_base_turkish_cased_qa_pipeline|
|Type:|pipeline|
|Compatibility:|Spark NLP 5.5.0+|
|License:|Open Source|
|Edition:|Official|
|Language:|tr|
|Size:|251.9 MB|

## References

https://huggingface.co/incidelen/distilbert-base-turkish-cased-qa

## Included Models

- MultiDocumentAssembler
- DistilBertForQuestionAnswering