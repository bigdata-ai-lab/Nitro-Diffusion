---
language:
- en
license: creativeml-openrail-m
thumbnail: "https://huggingface.co/nitrosocke/redshift-diffusion/resolve/main/images/redshift-diffusion-samples-01s.jpg"
tags:
- stable-diffusion
- text-to-image
- image-to-image

---
### Nitro Diffusion

Welcome to Nitro Diffusion - the first Multi-Style Model trained from scratch! This is a fine-tuned Stable Diffusion model trained on three artstyles simultaniously while keeping each style separate from the others. This allows for high control of mixing, weighting and single style use.
Use the tokens **_archer style, arcane style or modern diseny style_** in your prompts for the effect. You can also use more than one for a mixed style like in the examples down below:

**If you enjoy my work and want to test new models before release, please consider supporting me**
[![Become A Patreon](https://badgen.net/badge/become/a%20patron/F96854)](https://patreon.com/user?u=79196446)

**Single Style Characters from the model:**
![Videogame Samples](https://huggingface.co/nitrosocke/redshift-diffusion/resolve/main/images/redshift-diffusion-samples-01s.jpg)
**Multi Style Characters from the model:**
![Misc. Samples](https://huggingface.co/nitrosocke/redshift-diffusion/resolve/main/images/redshift-diffusion-samples-02s.jpg)
**Multi Style Scenes from the model:**
![Misc. Samples](https://huggingface.co/nitrosocke/redshift-diffusion/resolve/main/images/redshift-diffusion-samples-02s.jpg)

#### Prompt and settings for Tony Stark:
**(redshift style) robert downey jr as ironman Negative prompt: glasses helmet**
_Steps: 40, Sampler: DPM2 Karras, CFG scale: 7, Seed: 908018284, Size: 512x704_

#### Prompt and settings for the Ford Mustang:
**redshift style Ford Mustang**
_Steps: 20, Sampler: DPM2 Karras, CFG scale: 7, Seed: 579593863, Size: 704x512_

### 🧨 Diffusers

This model can be used just like any other Stable Diffusion model. For more information,
please have a look at the [Stable Diffusion](https://huggingface.co/docs/diffusers/api/pipelines/stable_diffusion).

You can also export the model to [ONNX](https://huggingface.co/docs/diffusers/optimization/onnx), [MPS](https://huggingface.co/docs/diffusers/optimization/mps) and/or [FLAX/JAX]().

```python
from diffusers import StableDiffusionPipeline
import torch

model_id = "nitrosocke/nitro-diffusion"
pipe = StableDiffusionPipeline.from_pretrained(model_id, torch_dtype=torch.float16)
pipe = pipe.to("cuda")

prompt = "archer arcane style magical princess with golden hair"
image = pipe(prompt).images[0]

image.save("./magical_princess.png")
```

This model was trained using the diffusers based dreambooth training by ShivamShrirao using prior-preservation loss and the _train-text-encoder_ flag in 11.000 steps.

## License

This model is open access and available to all, with a CreativeML OpenRAIL-M license further specifying rights and usage.
The CreativeML OpenRAIL License specifies: 

1. You can't use the model to deliberately produce nor share illegal or harmful outputs or content 
2. The authors claims no rights on the outputs you generate, you are free to use them and are accountable for their use which must not go against the provisions set in the license
3. You may re-distribute the weights and use the model commercially and/or as a service. If you do, please be aware you have to include the same use restrictions as the ones in the license and share a copy of the CreativeML OpenRAIL-M to all your users (please read the license entirely and carefully)
[Please read the full license here](https://huggingface.co/spaces/CompVis/stable-diffusion-license)


## Video Demos
#Batman
![Batman](https://huggingface.co/nitrosocke/Nitro-Diffusion/resolve/main/batman-demo-01.gif)
#Lara Croft
![Lara Croft](https://huggingface.co/nitrosocke/Nitro-Diffusion/resolve/main/laracroft-demo-01.gif)