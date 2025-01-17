---
layout: model
title: English image_classifier_convnext_tiny_224_local ConvNextForImageClassification
author: John Snow Labs
name: image_classifier_convnext_tiny_224_local
date: 2024-10-19
tags: [imagenet, image_classification, en, open_source, onnx, openvino]
task: Image Classification
language: en
edition: Spark NLP 5.5.0
spark_version: 3.0
supported: true
engine: openvino
annotator: ConvNextForImageClassification
article_header:
  type: cover
use_language_switcher: "Python-Scala-Java"
---

## Description

Pretrained ConvNext model for Image Classification, adapted from Hugging Face and curated to provide scalability and production-readiness using Spark NLP.

The ConvNeXT model was proposed in A ConvNet for the 2020s by Zhuang Liu, Hanzi Mao, Chao-Yuan Wu, Christoph Feichtenhofer, Trevor Darrell, Saining Xie.

## Predicted Entities



{:.btn-box}
<button class="button button-orange" disabled>Live Demo</button>
<button class="button button-orange" disabled>Open in Colab</button>
[Download](https://s3.amazonaws.com/auxdata.johnsnowlabs.com/public/models/image_classifier_convnext_tiny_224_local_en_5.5.0_3.0_1729378592800.zip){:.button.button-orange.button-orange-trans.arr.button-icon}
[Copy S3 URI](s3://auxdata.johnsnowlabs.com/public/models/image_classifier_convnext_tiny_224_local_en_5.5.0_3.0_1729378592800.zip){:.button.button-orange.button-orange-trans.button-icon.button-copy-s3}

## How to use



<div class="tabs-box" markdown="1">
{% include programmingLanguageSelectScalaPythonNLU.html %}
```python
image_assembler = ImageAssembler()     .setInputCol("image") \
    .setOutputCol("image_assembler")

imageClassifier = ConvNextForImageClassification \
    .pretrained("image_classifier_convnext_tiny_224_local", "en")    .setInputCols("image_assembler") \
    .setOutputCol("class")

pipeline = Pipeline(stages=[
    image_assembler,
    imageClassifier,
])

pipelineModel = pipeline.fit(imageDF)

pipelineDF = pipelineModel.transform(imageDF)
```
```scala
val imageAssembler = new ImageAssembler()
.setInputCol("image")
.setOutputCol("image_assembler")

val imageClassifier = ConvNextForImageClassification
.pretrained("image_classifier_convnext_tiny_224_local", "en")
.setInputCols("image_assembler")
.setOutputCol("class")

val pipeline = new Pipeline().setStages(Array(imageAssembler, imageClassifier))

val pipelineModel = pipeline.fit(imageDF)

val pipelineDF = pipelineModel.transform(imageDF)
```
</div>

{:.model-param}
## Model Information

{:.table-model}
|---|---|
|Model Name:|image_classifier_convnext_tiny_224_local|
|Compatibility:|Spark NLP 5.5.0+|
|License:|Open Source|
|Edition:|Official|
|Input Labels:|[image_assembler]|
|Output Labels:|[class]|
|Language:|en|
|Size:|107.4 MB|

## References

https://huggingface.co/facebook/convnext-tiny-224