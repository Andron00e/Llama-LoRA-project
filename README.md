# Fine-Tuning-project


  Here is my poject concerning fine-tuning of ML models. It consists of several parts mentioned below:
  * fine-tuning [openlm-research/open_llama_3b model](https://huggingface.co/openlm-research/open_llama_3b) using Low-Rank Adaptation technique (LoRA) on [OpenOrca](https://huggingface.co/datasets/Open-Orca/OpenOrca) Q&A dataset 
  * fine-tuning this very model using the same ubiquitous LoRA using my own dataset containing telegram messages, for more details follow next tips

## Llama-LoRA-Orca
You can see some details in my hf repo [Andron00e/YetAnother_Open-Llama-3B-LoRA-OpenOrca](https://huggingface.co/Andron00e/YetAnother_Open-Llama-3B-LoRA-OpenOrca)

## Llama-LoRA-Custom
Unfortunately an example of this model wouldn't be given, but there are some amusing details that shouldn't be missed

## Quality evaluation and results

* Fine-tuned on OpenOrca Open Llama 3B
  
|  Task   |Version | Metric |Value  |   |Stderr|
|---------|:------: |:--------|:-----: |:---:|:-----:|
|hellaswag|      0 |acc     |0.4899 |±  |0.0050|
|         |        |acc_norm|0.6506 |±  |0.0048|


* Fine-tuned on my custom dataset in russian language Open Llama 3B
  
|  Task   |Version| Metric |Value |   |Stderr|
|---------:|------:|--------|-----:|---|-----:|
|hellaswag|      0|acc     |0.4818|±  |0.0050|
|         |       |acc_norm|0.6377|±  |0.0048|


* Fine-tuned on mixed dataset (one part – Orca, second part – custom dataset)

|  Task   |Version| Metric |Value |   |Stderr|
|---------|------:|--------|-----:|---|-----:|
|hellaswag|      0|acc     |0..4618|±  |0.0050|
|         |       |acc_norm|0.6019|±  |0.0049|


* Fine-tuned on "wmt19", 'ru-en' dataset

|  Task   |Version| Metric |Value |   |Stderr|
|---------|------:|--------|-----:|---|-----:|
|hellaswag|      0|acc     |0.4817|±  |0.0050|
|         |       |acc_norm|0.6362|±  |0.0048|


## Citation
```bibtex
@software{openlm2023openllama,
  author = {Geng, Xinyang and Liu, Hao},
  title = {OpenLLaMA: An Open Reproduction of LLaMA},
  month = May,
  year = 2023,
  url = {https://github.com/openlm-research/open_llama}
}
```
```bibtex
@software{eval-harness,
  author       = {Gao, Leo and
                  Tow, Jonathan and
                  Biderman, Stella and
                  Black, Sid and
                  DiPofi, Anthony and
                  Foster, Charles and
                  Golding, Laurence and
                  Hsu, Jeffrey and
                  McDonell, Kyle and
                  Muennighoff, Niklas and
                  Phang, Jason and
                  Reynolds, Laria and
                  Tang, Eric and
                  Thite, Anish and
                  Wang, Ben and
                  Wang, Kevin and
                  Zou, Andy},
  title        = {A framework for few-shot language model evaluation},
  month        = sep,
  year         = 2021,
  publisher    = {Zenodo},
  version      = {v0.0.1},
  doi          = {10.5281/zenodo.5371628},
  url          = {https://doi.org/10.5281/zenodo.5371628}
}
```
```bibtex
@inproceedings{...,
  year={2020},
  title={Facebook FAIR's WMT19 News Translation Task Submission},
  author={Ng, Nathan and Yee, Kyra and Baevski, Alexei and Ott, Myle and Auli, Michael and Edunov, Sergey},
  booktitle={Proc. of WMT},
}
```
