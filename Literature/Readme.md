
# Literature
In this part, there will be four literature related to this research and I will explain how I am inspired by these literature and how I contribute to these literature.

#  The literature uses the same methods but answers different questions or limits to application scenarios. 
 1. "Interpretable Machine Learning: a Guide for Making Black Box Models Explainable" by Slack et al. (2019)

**Methodology:** Presented primarily as a review, the paper provides readers with a comprehensive guide to explaining black box models by combing through existing explainable machine learning (XAI) methods and techniques. The authors rely heavily on literature review, summarization and classification of existing XAI techniques in their methodology.

**Core Ideas:** The core idea of the paper is to provide a systematic approach to understanding and explaining black-box machine learning models. It emphasizes the importance of interpretability to facilitate wider adoption in real-world applications. The authors emphasize that XAI is not just an add-on, but a key component in building trustworthy and responsible AI systems.

**Contributions:** The main contribution of the paper is to provide readers with a comprehensive framework to help them understand and select different XAI approaches. By summarizing existing techniques, the paper provides guidance for researchers, engineers, and policy makers to ensure the interpretability of machine learning models.

**Future Perspectives:** The paper may refer to future directions in the field of XAI, which may include more advanced explanatory models, customized explanatory tools tailored to the needs of specific industries, and improvements in the balance between explanatory and performance. The discussion of future prospects helps guide the reader to new opportunities and challenges in XAI research.

2. "Sensitivity analysis: Strategies, methods, concepts, and challenges" by Pianosi, F., Sarrazin, F., & Wagener, T. (2022)

**Methodology**:

The methodology section of this article likely encompasses an extensive review and synthesis of existing literature on sensitivity analysis. Authors may have examined a wide range of strategies and methods employed in sensitivity analysis, emphasizing their application in environmental modeling. The article might also discuss the selection criteria for various sensitivity analysis methods and their appropriateness in different environmental contexts.

**Key Insights**:

The core insights of the article likely revolve around the identification and explanation of key strategies, methods, and concepts in sensitivity analysis. This could include discussions on the importance of sensitivity analysis in environmental modeling, the strengths and limitations of different approaches, and the conceptual underpinnings that guide the analysis of parameter influences.

**Contributions**:

The contributions of the article are likely twofold. Firstly, it may provide a comprehensive overview of sensitivity analysis, consolidating diverse strategies and methods into a cohesive framework. Secondly, the article may contribute insights into the challenges associated with sensitivity analysis in environmental modeling, offering potential solutions or avenues for future research. The synthesis of existing knowledge in this field could guide researchers and practitioners in making informed decisions regarding sensitivity analysis.

**Future Research**:

In addressing future research directions, the article might suggest areas that require further investigation or refinement. This could involve proposing new methodologies to overcome existing challenges in sensitivity analysis, identifying emerging trends in environmental modeling, or recommending avenues for integrating sensitivity analysis with other modeling techniques. By pinpointing gaps in current knowledge, the article may stimulate discussions on potential advancements and innovations in the field of sensitivity analysis within the context of environmental sciences.

# The literature addresses similar research questions but uses different methods or limits to different application scenarios.
To help the audience better understand Morris and SALib, I cite two related literature here.
1. **"SALib: An open-source Python library for Sensitivity Analysis" by Herman et al. (2017):**
   - **Methodology:** The paper details SALib, an open-source Python library for sensitivity analysis. The methodology consists mainly of a description of the design and implementation of SALib, as well as a comparison with other sensitivity analysis tools.
   - **Central Idea:** The central idea of the paper is to present the uses and flexibility of SALib, emphasizing its value in exploring the sensitivity of model outputs to input parameters.
   - **Contribution:** The contribution of the paper is to provide scientists and engineers with an easy-to-use tool for performing sensitivity analyses and to provide researchers with a way to understand the sources of uncertainty in models.
   - **Future Prospects:** The paper may discuss future directions for SALib, such as adding support for more model types and improving computational efficiency.

2. **"Exploring Sensitivity Analysis and Uncertainty Quantification Practices in Environmental Modelling" by Pianosi et al. (2016):**
   - **Methodology:** The paper may address the application of SALib and practical approaches to sensitivity analysis and uncertainty quantification in environmental modeling.
   - **Central Idea:** The paper is likely to emphasize the importance of analyzing parameter sensitivities of models in the field of environmental sciences and how tools such as SALib can be used to achieve this.
   - **Contribution:** The paper may have surveyed and summarized the application of SALib in the field of environmental science, providing lessons for researchers in other fields.
   - **Future Perspectives:** The paper may have explored the future development of sensitivity analyses in environmental modeling and made recommendations to improve and extend SALib.

#  The literature is limited to the same application scenario but uses different methods or answers other questions. 
"Global reconstruction of language models with linguistic rules – Explainable AI for online consumer reviews." By Binder et al. (2020)
**Introduction**:
Binder et al.(2020) focused on the language model. The focus of this paper lies in language models, particularly BERT, which are extensively utilized in text analytics tasks such as sentiment analysis. These models, however, pose a challenge as they are often perceived as opaque "black boxes," making their predictions difficult to comprehend. There is an emerging need for explainable AI (XAI) to deconstruct and rationalize predictions made by complex AI models, like BERT, to ensure compliance with regulations such as GDPR's "right to explanation."

**Motivation**:
Existing XAI methods for language models primarily concentrate on local, instance-specific reconstructions and lack strategies for achieving a global understanding of the model. This paper seeks to bridge this gap by introducing a novel global XAI approach that leverages linguistic rules to reconstruct BERT's predictions.

**Research Questions**:
RQ1: How can language model predictions be globally reconstructed using linguistic rules?

RQ2: How can the trade-off between fidelity and comprehensibility of global reconstructions be analyzed?

**Methods**:
The authors of the paper extract linguistic rules that are constructed using Natural Language Processing (NLP) building blocks such as Part-of-Speech (POS) tags and dependencies to reconstruct BERT's predictions. Fidelity and comprehensibility are evaluated using metrics like F1 score and the number of rules. Experiments are conducted, focusing on aspect and sentiment detection within online reviews.

**Results**:
The paper demonstrates that linguistic rules can successfully reconstruct BERT's predictions, achieving fidelity rates in the range of 78-82%. Depending on the specific objective, rule sets can be designed to emphasize either comprehensibility or fidelity. This illustrates that linguistic rules offer the potential for both high-fidelity and interpretable global reconstructions of language models. The paper also highlights the capability to balance the trade-off between fidelity and comprehensibility according to the requirements of a particular application.

**Relation to XAI**:
This paper introduces an innovative global, model-agnostic XAI approach tailored for complex neural language models like BERT. It illustrates how linguistic rules can provide interpretable global reconstructions, effectively opening the "black box," in alignment with the core goals of XAI. The analysis of the trade-off between fidelity and comprehensibility offers valuable insights for the design of XAI systems, enabling a balance that suits specific use cases.

Overall, this work significantly advances the XAI capabilities within a critical category of AI systems, namely neural language models.

**Theoretical aspect**
The theoretical aspect of my upcoming work involves developing models , using others' XAI structures and frameworks that aim to elucidate the decision-making processes of complex AI algorithms. These theories often focus on creating more interpretable representations and algorithms, bridging the gap between advanced machine learning techniques and human understanding.

**Empirical observation**
Empirical observation in my upcoming work encompasses the practical application of these theories in real-world scenarios. It involves collecting data on how users interact with AI systems and the challenges they face in understanding the AI's decisions. This empirical research helps identify the limitations and areas for improvement in explainability, refining theoretical models based on real-world use cases.

**Experimental investigation**
Experimental investigation in my upcoming work involves conducting controlled experiments to assess the effectiveness of different explainability techniques. Researchers may compare the interpretability of AI systems with and without XAI methods, measuring factors like user comprehension, trust, and decision accuracy. Through these experiments, the field aims to empirically validate and refine the theoretical models and inform the development of best practices for creating more transparent AI systems. Overall, XAI integrates these three aspects to foster a deeper understanding of AI models and improve their usability in various domains while addressing the "black box" problem.



## • How is your research similar to or built on the specific parts of the existing literature? How is your research advanced or different from the existing literature?
In the software I wrote alone, I implemented the analysis of the parameter weights in the model, using the SALib database. My research was inspired by three previously mentioned papers, "Interpretable Machine Learning: A Guide for Making Black Box Models Explainable", "SALib: An open-source Python library for Sensitivity Analysis", "SALib: An open-source Python library for Sensitivity Analysis", and "Exploring Sensitivity Analysis and Uncertainty Quantification Practices in Environmental Modelling".

All three papers have commonalities in exploring interpretive and sensitivity analysis in machine learning. First, they all focus on the interpretability of the parameters in the model, emphasizing the importance of understanding the relationship between the model output and the input parameters. This is relevant to my research as I focus on analyzing the weights of the parameters in a model to reveal their impact on the model output. This common focus on interpretability has led to my interest in building software that can reveal the internal mechanisms of a model.

Also, the use of the SALib library was part of my research inspiration." The paper "SALib: An open-source Python library for Sensitivity Analysis" details the design and implementation of SALib as a powerful tool for performing sensitivity analysis. I was so inspired by it that I decided to implement my software using the SALib database in order to perform the analysis of parameter weights more easily and efficiently.

However, although my research was inspired by the aforementioned paper, I also made some contributions in terms of innovation. My software not only focuses on sensitivity analysis, but also looks at deeply analyzing the weights of each parameter in the model. By implementing a detailed analysis of the weights, I enable the user to get a fuller picture of how the model works. In addition, I have included some customization features to improve the user experience and applicability of the software. This innovation of in-depth parsing and enhanced functionality is unique to my research.

Taken together, my research provides a new approach to comprehensive, in-depth parsing of model parameter weights based on explanatory and sensitivity analysis by combining the SALib library and customization features. This comprehensive analysis helps users to better understand the internal mechanisms of the model and thus make more informed decisions in real-world applications.

# Contribution to literature

### To "SALib: An open-source Python library for Sensitivity Analysis" by Herman et al. (2017)

**Practical Application Scenarios:** Going beyond theoretical exploration, my study successfully applies the Morris algorithm and SALib to various practical domains. By conducting case studies in environmental science, medicine, and finance, I have enriched the practical application experience of these tools, expanding their relevance to real-world problems.

### To "Global reconstruction of language models with linguistic rules – Explainable AI for online consumer reviews." By Binder et al. (2020)

**Exploring New Research Avenues:** The paper outlines new research directions within the global sensitivity analysis field. These directions include exploring more efficient parameter sensitivity assessment methods, deepening interdisciplinary collaborations, and identifying potential applications in emerging fields. This provides researchers with guidance on the future development of the field.

**Practical Guides:** The research includes detailed practical guides, offering step-by-step operational procedures, solutions to common issues, and best practices for leveraging the Morris algorithm and SALib in real-world scenarios. These guides enhance the feasibility and usability of these tools for practical applications.

**Algorithm Performance Evaluation:** Comprehensive evaluations of the Morris algorithm and SALib performance have been conducted, considering various datasets, parameter configurations, and application scenarios. These evaluations not only serve as references for other researchers in tool selection but also guide further optimization of their performance in real-world applications.

### To "Interpretable Machine Learning: a Guide for Making Black Box Models Explainable" by Slack et al. (2019)

**Interdisciplinary Integration:** The study not only delves vertically into the Morris algorithm and SALib but also horizontally integrates them into multiple disciplinary domains. This interdisciplinary fusion fosters collaboration across different fields, opening up new opportunities for cross-disciplinary research in the global sensitivity analysis domain and facilitating knowledge integration and innovation.

# Limitation
Currently this model can only be used to make a detection on the base model but this model is not able to make an accurate detection on some of the models such as CNN and KNN.These models have been detected during the training as not being able to be applied to my research and in the future these models will also be covered in order to improve my model.

### Abstract

<img src="04367898f3f93984e2c18fb4255279a.jpg" alt="Abstract Word Cloud">


# Reference


```
@article{binder2022global,
  title={Global reconstruction of language models with linguistic rules--Explainable AI for online consumer reviews},
  author={Binder, Markus and Heinrich, Bernd and Hopf, Marcus and Schiller, Alexander},
  journal={Electronic Markets},
  volume={32},
  number={4},
  pages={2123--2138},
  year={2022},
  publisher={Springer}
}

@inproceedings{caruana2015intelligible,
  title={Intelligible models for healthcare: Predicting pneumonia risk and hospital 30-day readmission},
  author={Caruana, Rich and Lou, Yin and Gehrke, Johannes and Koch, Paul and Sturm, Marc and Elhadad, Noemie},
  booktitle={Proceedings of the 21th ACM SIGKDD international conference on knowledge discovery and data mining},
  pages={1721--1730},
  year={2015}
}

@article{lundberg2017unified,
  title={A unified approach to interpreting model predictions},
  author={Lundberg, Scott M and Lee, Su-In},
  journal={Advances in neural information processing systems},
  volume={30},
  year={2017}
}

@article{shi2018structural,
  title={Structural estimation of behavioral heterogeneity},
  author={Shi, Zhentao and Zheng, Huanhuan},
  journal={Journal of Applied Econometrics},
  volume={33},
  number={5},
  pages={690--707},
  year={2018},
  publisher={Wiley Online Library}
}

@article{rudin2019stop,
  title={Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead},
  author={Rudin, Cynthia},
  journal={Nature machine intelligence},
  volume={1},
  number={5},
  pages={206--215},
  year={2019},
  publisher={Nature Publishing Group UK London}
}```
