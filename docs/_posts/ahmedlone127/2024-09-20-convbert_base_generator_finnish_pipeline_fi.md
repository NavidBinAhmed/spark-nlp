---
layout: model
title: Finnish convbert_base_generator_finnish_pipeline pipeline BertEmbeddings from Finnish-NLP
author: John Snow Labs
name: convbert_base_generator_finnish_pipeline
date: 2024-09-20
tags: [fi, open_source, pipeline, onnx]
task: Embeddings
language: fi
edition: Spark NLP 5.5.0
spark_version: 3.0
supported: true
annotator: PipelineModel
article_header:
  type: cover
use_language_switcher: "Python-Scala-Java"
---

## Description

Pretrained BertEmbeddings, adapted from Hugging Face and curated to provide scalability and production-readiness using Spark NLP.`convbert_base_generator_finnish_pipeline` is a Finnish model originally trained by Finnish-NLP.

{:.btn-box}
<button class="button button-orange" disabled>Live Demo</button>
<button class="button button-orange" disabled>Open in Colab</button>
[Download](https://s3.amazonaws.com/auxdata.johnsnowlabs.com/public/models/convbert_base_generator_finnish_pipeline_fi_5.5.0_3.0_1726806379722.zip){:.button.button-orange.button-orange-trans.arr.button-icon}
[Copy S3 URI](s3://auxdata.johnsnowlabs.com/public/models/convbert_base_generator_finnish_pipeline_fi_5.5.0_3.0_1726806379722.zip){:.button.button-orange.button-orange-trans.button-icon.button-copy-s3}

## How to use



<div class="tabs-box" markdown="1">
{% include programmingLanguageSelectScalaPythonNLU.html %}
```python

pipeline = PretrainedPipeline("convbert_base_generator_finnish_pipeline", lang = "fi")
annotations =  pipeline.transform(df)   

```
```scala

val pipeline = new PretrainedPipeline("convbert_base_generator_finnish_pipeline", lang = "fi")
val annotations = pipeline.transform(df)

```
</div>

{:.model-param}
## Model Information

{:.table-model}
|---|---|
|Model Name:|convbert_base_generator_finnish_pipeline|
|Type:|pipeline|
|Compatibility:|Spark NLP 5.5.0+|
|License:|Open Source|
|Edition:|Official|
|Language:|fi|
|Size:|181.3 MB|

## References

https://huggingface.co/Finnish-NLP/convbert-base-generator-finnish

## Included Models

- DocumentAssembler
- TokenizerModel
- BertEmbeddings