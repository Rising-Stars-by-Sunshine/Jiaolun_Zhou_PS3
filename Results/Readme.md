<img src="Research questions.png" alt="Abstract Word Cloud">

# Answer to research questions
### Research Question 1: How can SALib be used to analyze the comparison of weights for different parameters in analyzing the problem of AI?

SALib proves instrumental in unraveling the intricacies of parameter importance in AI models. Leveraging the Morris method from SALib, I conducted a sensitivity analysis on my black-box model. This involved systematically varying input parameters to discern their impact on the model's output. The obtained weightings for each parameter offer valuable insights into their relative significance, guiding the understanding of feature importance in the AI context. The Morris method's efficiency and versatility, as embedded in SALib, allowed for a robust analysis, aiding in the interpretation and optimization of the studied AI model.

### Research Question 2: Can Morris be used in analyzing other comparison of weights for different parameters in other models or using other datas?

The applicability of the Morris method extends beyond the confines of my specific AI model. It serves as a powerful tool for analyzing parameter weights in various models across different datasets. The versatility of the Morris method, as implemented in SALib, facilitates its application to diverse scenarios, including other machine learning models like CNN and KNN. However, it's essential to acknowledge potential limitations and variations in model architectures, data characteristics, and research objectives. While SALib's Morris method offers a valuable and generic approach, adjustments may be necessary to address specific nuances in different models or datasets.

### Limitations and Future Considerations:

Despite successfully utilizing SALib for AI model sensitivity analysis, limitations emerged when applying the software to CNN and KNN. This underscores a potential constraint in the adaptability of the Morris method to certain model architectures. Understanding these limitations is crucial for refining the methodology. Future research should explore tailored approaches for sensitivity analysis in deep learning models, considering their unique structures and complexities. This acknowledgment sets the stage for further advancements in sensitivity analysis methodologies, ensuring their relevance and effectiveness across a broader spectrum of AI models.

# Reference
Binder, M., Heinrich, B., Hopf, M., et al. (2022). "Global reconstruction of language models with linguistic rules – Explainable AI for online consumer reviews." Electron Markets, 32, 2123–2138.

Caruana, R., Lou, Y., Gehrke, J., Koch, P., Sturm, M., & Elhadad, N. (2015). "Intelligible models for healthcare: Predicting pneumonia risk and hospital 30-day readmission." In Proceedings of the 21th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (pp. 1721-1730)

Lundberg, S. M., & Lee, S. I. (2017). "A unified approach to interpreting model predictions." In Advances in neural information processing systems (pp. 4765-4774)

Chen, J., Song, L., Le, G., & Samaras, D. (2018). "Local Interpretable Model-Agnostic Explanations for Black Box Models." arXiv preprint arXiv:1802.03735

Rudin, C. (2019). "Stop explaining black box machine learning models for high stakes decisions and use interpretable models instead." Nature Machine Intelligence, 1(5), 206-215

Broussard, Meredith . “Artificial Unintelligence.” MIT Press, 29 Sept. 2020, mitpress.mit.edu/9780262537018/artificial-unintelligence/.
