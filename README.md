# Multilingual Jailbreak Challenges in Large Language Models

<p align="center" style="display: flex; flex-direction: row; justify-content: center; align-items: center">
📄 <a href="https://arxiv.org/abs/2310.06474" target="_blank" style="margin-right: 15px; margin-left: 10px">Paper</a> • 
🤗 <a href="https://huggingface.co/datasets/DAMO-NLP-SG/MultiJail" target="_blank" style="margin-left: 10px">Dataset</a> 
</p>

This repo contains the data for our paper ["Multilingual Jailbreak Challenges in Large Language Models"](https://arxiv.org/abs/2310.06474).

## Annotation Statistics
We collected a total of 315 English unsafe prompts and annotated them into nine non-English languages. The languages were categorized based on resource availability, as shown below:

**High-resource languages:** Chinese (zh), Italian (it), Vietnamese (vi)

**Medium-resource languages:** Arabic (ar), Korean (ko), Thai (th)

**Low-resource languages:** Bengali (bn), Swahili (sw), Javanese (jv)


## Introduction
![](./figure/introduction.jpg)
We identify the presence of multilingual jailbreak challenges within LLMs and propose to study them under two potential scenarios: unintentional and intentional. The unintentional scenario involves users querying LLMs using non-English prompts and inadvertently bypassing the safety mechanisms, while the intentional scenario concerns malicious users combining malicious instructions with multilingual prompts to attack LLMs deliberately.


## Dataset
We carefully gather English harmful queries and manually translate them by native speakers into 9 non-English languages, ranging from high-resource to low-resource. This leads us to the creation of the first multilingual jailbreak dataset called MultiJail. The prompt in this dataset can directly serve for the unintentional scenario, while we also simulate intentional scenario by combining the prompt with an English malicious instruction.


The language categories and their corresponding languages are as follows: High-resource: Chines (zh), Italic (it), Vietnamese (vi); Medium-resource: Arabic (ar), Korean (ko), Thai (th); Low-resource: Bengali (bn), Swahili (sw), Javanese (jv).

The malicious instruction used in this work is [AIM](https://www.jailbreakchat.com/prompt/4f37a029-9dff-4862-b323-c96a5504de5d).

## Result
![](./figure/result.jpg)

## Self-Defence
To handle such a challenge in the multilingual context, we propose a novel Self-Defence framework that automatically generates multilingual training data for safety fine-tuning.

![](./figure/algo.jpg)

Experimental results show that ChatGPT fine-tuned with such data can achieve a substantial reduction in unsafe content generation.

![](./figure/self-defence-result.jpg)

## Ethics Statement
Our research investigates the safety challenges of LLMs in multilingual settings. We are aware of the potential misuse of our findings and emphasize that our research is solely for academic purposes and ethical use. Misuse or harm resulting from the information in this paper is strongly discouraged. To address the identified risks and vulnerabilities, we commit to open-sourcing the data used in our study. This openness aims to facilitate vulnerability identification, encourage discussions, and foster collaborative efforts to enhance LLM safety in multilingual contexts. Furthermore, we have developed the SELF-DEFENSE framework to address multilingual jailbreak challenges in LLMs. This framework automatically generates multilingual safety training data to mitigate risks associated with unintentional and intentional jailbreak scenarios. Overall, our work not only highlights multilingual jailbreak challenges in LLMs but also paves the way for future research, collaboration, and innovation to enhance their safety.

## Citation
```
@misc{deng2023multilingual,
      title={Multilingual Jailbreak Challenges in Large Language Models}, 
      author={Yue Deng and Wenxuan Zhang and Sinno Jialin Pan and Lidong Bing},
      year={2023},
      eprint={2310.06474},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```
