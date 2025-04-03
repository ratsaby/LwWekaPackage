# LwWekaPackage

Large-Width (LW) algorithm is a type of lazy learning for data classification, see M. Anthony and J. Ratsaby, Large-width machine learning algorithm, *Progress in Artificial Intelligence* (2020).
 
It operates with the aim of maintaining a large sample width (which is a notion similar to sample margin). Given a sample of labeled and unlabeled examples  it iteratively picks the  next unlabeled example and classifies it while maintaining  a large distance between each labeled example and its nearest unlike-prototype (a prototype is either a labeled example or an unlabeled example which has already been classified).  In this iterative process, the algorithm gives a higher priority to  unlabeled points whose classification decision `interferes' less with the labeled sample. Compared to other  large-margin learning algorithms such as the ubiquitous  SVM kernel methods,  where a kernel function needs to be defined and be an inner product in some higher dimensional space, the LW algorithm can use any distance function, which does not have to satisfy anything other than non-negativity (it need not even satisfy the triangle inequality). This makes LW easy to apply in classification learning problems on general distance spaces. In the current WEKA implementation, the distance function is Euclidean hence the data needs to be numeric. It has been tested with the WEKA Explorer and Experimenter and also with remote engines.



### 📖 Citation

To cite this work:
<pre> 
```bibtex @article{AnthonyRatsaby2020, author = {M. Anthony and J. Ratsaby}, doi = {10.1007/s13748-020-00212-4}, journal = {Progress in Artificial Intelligence}, number = {3}, pages = {275--285}, title = {Large-width machine learning algorithm}, url = {https://doi.org/10.1007/s13748-020-00212-4}, volume = {9}, year = {2020} } ```
</pre>
