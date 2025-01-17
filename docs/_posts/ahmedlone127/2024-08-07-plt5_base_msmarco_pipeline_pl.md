---
layout: model
title: Polish plt5_base_msmarco_pipeline pipeline T5Transformer from clarin-knext
author: John Snow Labs
name: plt5_base_msmarco_pipeline
date: 2024-08-07
tags: [pl, open_source, pipeline, onnx]
task: [Question Answering, Summarization, Translation, Text Generation]
language: pl
edition: Spark NLP 5.4.2
spark_version: 3.0
supported: true
annotator: PipelineModel
article_header:
  type: cover
use_language_switcher: "Python-Scala-Java"
---

## Description

Pretrained T5Transformer, adapted from Hugging Face and curated to provide scalability and production-readiness using Spark NLP.`plt5_base_msmarco_pipeline` is a Polish model originally trained by clarin-knext.

{:.btn-box}
<button class="button button-orange" disabled>Live Demo</button>
<button class="button button-orange" disabled>Open in Colab</button>
[Download](https://s3.amazonaws.com/auxdata.johnsnowlabs.com/public/models/plt5_base_msmarco_pipeline_pl_5.4.2_3.0_1723059087570.zip){:.button.button-orange.button-orange-trans.arr.button-icon}
[Copy S3 URI](s3://auxdata.johnsnowlabs.com/public/models/plt5_base_msmarco_pipeline_pl_5.4.2_3.0_1723059087570.zip){:.button.button-orange.button-orange-trans.button-icon.button-copy-s3}

## How to use



<div class="tabs-box" markdown="1">
{% include programmingLanguageSelectScalaPythonNLU.html %}
```python

pipeline = PretrainedPipeline("plt5_base_msmarco_pipeline", lang = "pl")
annotations =  pipeline.transform(df)   

```
```scala

val pipeline = new PretrainedPipeline("plt5_base_msmarco_pipeline", lang = "pl")
val annotations = pipeline.transform(df)

```
</div>

{:.model-param}
## Model Information

{:.table-model}
|---|---|
|Model Name:|plt5_base_msmarco_pipeline|
|Type:|pipeline|
|Compatibility:|Spark NLP 5.4.2+|
|License:|Open Source|
|Edition:|Official|
|Language:|pl|
|Size:|1.2 GB|

## References

https://huggingface.co/clarin-knext/plt5-base-msmarco

## Included Models

- DocumentAssembler
- T5Transformer