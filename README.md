---
library_name: peft
base_model: Hugofernandez/Mistral-7B-v0.1-colab-sharded
---
# load perf model
from peft import PeftModel, PeftConfig
from transformers import AutoModelForCausalLM

config = PeftConfig.from_pretrained("Kamilatr/mistral_model")
model = AutoModelForCausalLM.from_pretrained("Hugofernandez/Mistral-7B-v0.1-colab-sharded")
model = PeftModel.from_pretrained(model, "Kamilatr/mistral_model")

- PEFT 0.7.1
