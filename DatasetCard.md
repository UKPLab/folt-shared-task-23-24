# Dataset description

This dataset contains 850 annotated LLM answers for 130 CCAs. For each CCA, we collect five answers from different LLMs (Llama-2-70b-chat with two different system instructions, OpenAI ChatGPT, Microsoft BingChat, and PerplexityAI). It is important to note that some LLM responses have multiple annotations, contributed by different team members.

# Dataset structure
1. the data section
- doi: the original CCA doi, such as "10.1002/cca.3617"
- question: the question from the original CCA
- gold_answer: the original answer written by the professional experts
- url: the original CCA url
- llm_answer: the answer from an LLM
- llm_answer_ref: the reference information from an LLM when applicable (this applies to BingChat and PerplexityAI in our setting)
- llm_model_name: the id of an LLM model that generates llm_answer and llm_answer_ref, such as "bingchat_prompt0_answer"
- llm_model_prompt: the raw prompt we used to prompt LLMs
- topic1: the subject area to which A CCA is related
- topic2: the more fine-grained subject area to which a CCA is related
- year: the year in which a CCA was created
- author: the professional expert's name who provide the gold answer for a CCA quetion

2. the annotation result section that is associated with a data section
- id: the annotation unit id. It could be the whole answer level, such as "10-1002_cca-3617_bingchat_prompt0_answer", or a single sentence from an LLM answer, such as "10-1002_cca-3617_bingchat_prompt0_answer_sent0"
- from_name: label studio annotation configurate field 
- to_name: label studio annotation configurate field
- type: the annotation type. For the whole answer level, the value is "choices", which indicates whether the whole LLM answer is relevent to the question ("Valid") or not ("Invalid"). For the single sentence level, the value is "labels", which indicates the category (e.g., "Contradiction") of a sentence from an LLM answer. For the labels value that indicates annotations of individual sentences from an LLM answer, the start position (e.g., "0"), end position (e.g., "150"), as well as the corresponding text (e.g., "Intermittent fasting may be effective in reducing weight when compared to ad libitum feeding and may be as effective as continuous energy restriction") are also included. 
  

  
# Dataset contributors 
We express our gratitude to the participants of the FoLT 2023/2024 course shared task, who generously contributed their annotations for future teaching and research purposes. Below is a list of the students who contributed to this dataset and agreed to have their names listed in the dataset card (names are in alphabetical order):

- Chahid El Aaouadi	
- Daniel Martins	
- Florian Steigleder	
- Gabriel Thiem	
- Jenni Ellwanger	
- Jennifer Toebe	
- Julia Perathoner	
- Leon Krüger	
- Martin Ruzicka	
- Nehath Nils Mia	
- Nathan Schrodt	
- Nils Waldraff	
- Zelal Cicek Tacyildiz	
  
