---
layout: model
title: Latin roberta_base_latin_v2_pipeline pipeline RoBertaEmbeddings from ClassCat
author: John Snow Labs
name: roberta_base_latin_v2_pipeline
date: 2024-09-11
tags: [la, open_source, pipeline, onnx]
task: Embeddings
language: la
edition: Spark NLP 5.5.0
spark_version: 3.0
supported: true
annotator: PipelineModel
article_header:
  type: cover
use_language_switcher: "Python-Scala-Java"
---

## Description

Pretrained RoBertaEmbeddings, adapted from Hugging Face and curated to provide scalability and production-readiness using Spark NLP.`roberta_base_latin_v2_pipeline` is a Latin model originally trained by ClassCat.

{:.btn-box}
<button class="button button-orange" disabled>Live Demo</button>
<button class="button button-orange" disabled>Open in Colab</button>
[Download](https://s3.amazonaws.com/auxdata.johnsnowlabs.com/public/models/roberta_base_latin_v2_pipeline_la_5.5.0_3.0_1726093841809.zip){:.button.button-orange.button-orange-trans.arr.button-icon}
[Copy S3 URI](s3://auxdata.johnsnowlabs.com/public/models/roberta_base_latin_v2_pipeline_la_5.5.0_3.0_1726093841809.zip){:.button.button-orange.button-orange-trans.button-icon.button-copy-s3}

## How to use



<div class="tabs-box" markdown="1">
{% include programmingLanguageSelectScalaPythonNLU.html %}
```python

pipeline = PretrainedPipeline("roberta_base_latin_v2_pipeline", lang = "la")
annotations =  pipeline.transform(df)   

```
```scala

val pipeline = new PretrainedPipeline("roberta_base_latin_v2_pipeline", lang = "la")
val annotations = pipeline.transform(df)

```
</div>

{:.model-param}
## Model Information

{:.table-model}
|---|---|
|Model Name:|roberta_base_latin_v2_pipeline|
|Type:|pipeline|
|Compatibility:|Spark NLP 5.5.0+|
|License:|Open Source|
|Edition:|Official|
|Language:|la|
|Size:|465.2 MB|

## References

https://huggingface.co/ClassCat/roberta-base-latin-v2

## Included Models

- DocumentAssembler
- TokenizerModel
- RoBertaEmbeddings