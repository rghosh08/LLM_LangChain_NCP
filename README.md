# 🎓 Develop private LLM application on Nutanix Cloud Platform


Large Language Models (LLMs), based on the transformer architecture, like GPT, T5, and BERT,  have achieved state-of-the-art (SOTA) results in various Natural Language Processing (NLP) tasks especially for text generation and conversational bots. The real benefits of LLMs can be tapped only when they can be translated into applications which generate end-user values. An LLM application development involves LLM service, data connectors, raw data to prompt converter template, output parsing, and operationalizing auxiliary services such as vector databases, message queue, and others. As applications become more heterogeneous, an LLM application becomes prohibitively complex with multiple moves pieces. Another design challenge comes from data security with many LLM apps depending on third-party API services from organizations such as OpenAI, Hugging Face. In this scenario, zero-trust organizations such as banks, hospitals, and similar organizations demand security posture hardening by running the LLM models private and eliminating the need for the third-party API services. In this context, LangChain is a prevalent orchestration platform to glue together different application components. 
In this article, we present how a private LLM application can be developed using LangChain on Nutanix Cloud Platform (NCP) which is optimized for easy manageability and resiliency with the state-of-the-art AI infrastructure including high-performance GPU, fast NVMe, and storage scaling. 




## 🔍 Main Findings

We also cover LLM benchmarking in the context of the evaluation of our QA app. We evaluate the QA app with 10 different prompts covering seven different logical patterns for five architectures of flan-T5 models. We also come up with an empirical recommendation policy for model selection depending on the QA type. 

## 🚀 Reproducing the Results

You can directly run the `main.ipynb` to recreate the results. 


## 💾 Datasets and Generations

For this simple case study, datasets are simply kept in two inline arrays.

```
prompts = [
    'What is the capital of the United States of America?',
    'What is the capital of India?',
    'What is the capital of China?',
    'What is the next number in the sequence: 1, 1, 2, 3, 5, 8, ...? If all cats have tails, and Fluffy is a cat, does Fluffy have a tail?',
    'If you eat too much junk food, what will happen to your health? How does smoking affect the risk of lung cancer?',
    'In the same way that pen is related to paper, what is fork related to? If tree is related to forest, what is brick related to?',
    'Every time John eats peanuts, he gets a rash. Does John have a peanut allergy? Every time Sarah studies for a test, she gets an A. Will Sarah get an A on the next test if she studies?',
    'All dogs have fur. Max is a dog. Does Max have fur? If it is raining outside, and Mary does not like to get wet, will Mary take an umbrella?',
    'If I had studied harder, would I have passed the exam? What would have happened if Thomas Edison had not invented the light bulb?',
    'The center of Tropical Storm Arlene, at 02/1800 UTC, is near 26.7N 86.2W. This position is about 425 km/230 nm to the west of Fort Myers in Florida, and it is about 550 km/297 nm to the NNW of the western tip of Cuba. The tropical storm is moving southward, or 175 degrees, 4 knots. The estimated minimum central pressure is 1002 mb. The maximum sustained wind speeds are 35 knots with gusts to 45 knots. The sea heights that are close to the tropical storm are ranging from 6 feet to a maximum of 10 feet.  Precipitation: scattered to numerous moderate is within 180 nm of the center in the NE quadrant. Isolated moderate is from 25N to 27N between 80W and 84W, including parts of south Florida.  Broad surface low pressure extends from the area of the tropical storm, through the Yucatan Channel, into the NW part of the Caribbean Sea.   Where and when will the storm make landfall?'
]

types = [
    'Knowledge Retrieval',
    'Knowledge Retrieval',
    'Knowledge Retrieval',
    'Logical Reasoning',
    'Cause and Effect',
    'Analogical Reasoning',
    'Inductive Reasoning',
    'Deductive Reasoning',
    'Counterfactual Reasoning',
    'In Context'
]
```



## 📚 Read More


* [**LangChain**](https://python.langchain.com/docs/get_started/introduction.html)
* [**Nutanix Cloud Platform**](https://www.nutanix.com/products)
* [**Flan-T5**](https://huggingface.co/docs/transformers/model_doc/flan-t5)

## 🎯 Reference


```
@article{chung2022scaling,
  title={Scaling instruction-finetuned language models},
  author={Chung, Hyung Won and Hou, Le and Longpre, Shayne and Zoph, Barret and Tay, Yi and Fedus, William and Li, Eric and Wang, Xuezhi and Dehghani, Mostafa and Brahma, Siddhartha and others},
  journal={arXiv preprint arXiv:2210.11416},
  year={2022}
}
```