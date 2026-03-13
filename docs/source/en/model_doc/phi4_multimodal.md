<!--Copyright 2025 The HuggingFace Team. All rights reserved.
Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with
the License. You may obtain a copy of the License at
http://www.apache.org/licenses/LICENSE-2.0
Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on
an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.
⚠️ Note that this file is in Markdown but contain specific syntax for our doc-builder (similar to MDX) that may not be
rendered properly in your Markdown viewer.
-->
*This model was released on 2025-03-03 and added to Hugging Face Transformers on 2025-03-25.*

<div style="float: right;">
  <div class="flex flex-wrap space-x-1">
    <img alt="PyTorch" src="https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white&style=flat">
  </div>
</div>

## Phi4 Multimodal

[Phi4 Multimodal](https://huggingface.co/papers/2503.01743) is a multimodal model capable of text, image, and speech and audio inputs or any combination of these. It features a mixture of LoRA adapters for handling different inputs, and each input is routed to the appropriate encoder.

You can find all the original Phi4 Multimodal checkpoints under the [Phi4](https://huggingface.co/collections/microsoft/phi-4-677e9380e514feb5577a40e4) collection.

> [!TIP]
> This model was contributed by [cyrilvallez](https://huggingface.co/cyrilvallez).
>
> Click on the Phi-4 Multimodal in the right sidebar for more examples of how to apply Phi-4 Multimodal to different tasks.

The example below demonstrates how to generate text based on an image with [`Pipeline`] or the [`AutoModel`] class.

<hfoptions id="usage">
<hfoption id="Pipeline">

```python
from transformers import pipeline
generator = pipeline("text-generation", model="microsoft/Phi-4-multimodal-instruct", dtype="auto", device=0)

prompt = "Explain the concept of multimodal AI in simple terms."

result = generator(prompt, max_length=50)
print(result[0]['generated_text'])
```

</hfoption>
<hfoption id="AutoModel">

```py runnable:test_doc_1
# pytest-decorator: transformers.testing_utils.slow, transformers.testing_utils.require_torch

```

</hfoption>
</hfoptions>

## Notes

The example below demonstrates inference with an audio and text input.

```py runnable:test_doc_2
# pytest-decorator: transformers.testing_utils.slow, transformers.testing_utils.require_torch

```

## Phi4MultimodalFeatureExtractor

[[autodoc]] Phi4MultimodalFeatureExtractor

## Phi4MultimodalImageProcessorFast

[[autodoc]] Phi4MultimodalImageProcessorFast

## Phi4MultimodalProcessor

[[autodoc]] Phi4MultimodalProcessor
    - __call__

## Phi4MultimodalAudioConfig

[[autodoc]] Phi4MultimodalAudioConfig

## Phi4MultimodalVisionConfig

[[autodoc]] Phi4MultimodalVisionConfig

## Phi4MultimodalConfig

[[autodoc]] Phi4MultimodalConfig

## Phi4MultimodalAudioModel

[[autodoc]] Phi4MultimodalAudioModel

## Phi4MultimodalVisionModel

[[autodoc]] Phi4MultimodalVisionModel

## Phi4MultimodalModel

[[autodoc]] Phi4MultimodalModel
    - forward

## Phi4MultimodalForCausalLM

[[autodoc]] Phi4MultimodalForCausalLM
    - forward
