# LwWekaPackage

This [file](LW.zip) is a package for  [WEKA](https://ml.cms.waikato.ac.nz/weka) that implements a machine learning algorithm called
Large-Width (LW),  by [Martin Anthony](https://www.lse.ac.uk/Mathematics/people/Martin-Anthony) and [Joel Ratsaby](https://tinyurl.com/ratsaby), Large-width machine learning algorithm, *Progress in Artificial Intelligence* (2020).
It belongs to the category of 'lazy learning' for data classification as there is no model generated and it makes its decision based on the data alone.

## Overview of the algorithm
 
It operates to maintain a large sample width (which is a notion similar to sample margin). Given a sample of labeled and unlabeled examples, it iteratively picks the next unlabeled example and classifies it while maintaining a large distance between each labeled example and its nearest unlike-prototype (a prototype is either a labeled example or an unlabeled example that has already been classified). In this iterative process, the algorithm prioritizes unlabeled points whose classification decision `interferes' less with the labeled sample. It stops when all the unlabeled examples are classified. 

Compared to other large-margin learning algorithms such as the ubiquitous SVM kernel methods, where a kernel function needs to be defined and be an inner product in some higher dimensional space, the LW algorithm can use any distance function, which does not have to satisfy anything other than non-negativity (for instance, it need not  satisfy the triangle inequality). This makes LW easy to apply in classification learning problems on general distance spaces.

## Implementation

On WEKA, the algorithm treats the Training set as the labeled examples and the Test set as the unlabeled examples, but when applied in the real world, it can learn from a single set consisting of a mixture of labeled and unlabeled examples.

## Limitation 
In the current WEKA implementation, the distance function is Euclidean hence the data needs to be numeric. It has been tested with the WEKA Explorer and Experimenter and also with remote engines.

## Platforms
The package runs on Linux, Mac OS, and Windows

## 📖 Citation

Bibtex
<br>
<pre> ``` @article{AnthonyRatsaby2020, author = {M. Anthony and J. Ratsaby}, doi = {10.1007/s13748-020-00212-4}, journal = {Progress in Artificial Intelligence}, number = {3}, pages = {275--285}, title = {Large-width machine learning algorithm}, url = {https://doi.org/10.1007/s13748-020-00212-4}, volume = {9}, year = {2020} } ```</pre>

## Installing the package

Click on the link [file](LW.zip) then on the top right click the three dots, and choose download. Then  install it from the package manager of WEKA.

If you are updating this package form an older to a newer version, make sure first to delete the folder /tmp/lw-weka/
