This project explores the Leukemia dataset from OpenML using a mix of dimensionality reduction, clustering, and classification techniques. The main idea is to simplify the high-dimensional data with Non-negative Matrix Factorization (NMF), check how stable the clusters are using the Cophenetic Correlation Coefficient (CCC), and then use the reduced features to train a Support Vector Machine (SVM) classifier.

By combining these steps, the project shows how unsupervised learning (NMF and clustering) can work together with supervised learning (SVM) to both understand the structure of the data and make accurate predictions. The implementation is done in Python with libraries like NumPy, Pandas, Scikit-learn, and Matplotlib.
The results highlight that NMF provides meaningful low-dimensional features, the CCC helps identify the best number of clusters, and SVM achieves good accuracy when trained on these reduced features. This makes the workflow useful for analyzing biomedical datasets and can be further improved by trying other reduction methods, testing different classifiers, or applying it to new datasets.Results

RESULTS:
- Generated CCC plots -- to determine the stability of clusters.  
- Found the optimal `K` for NMF factorization.  
- Achieved strong classification accuracy using SVM on reduced features.

Project Workflow
1. Data Loading
   - Fetch the Leukemia dataset from OpenML.  

2. Preprocessing 
   - Scale features using MinMaxScaler.  
   - Prepare data for factorization and clustering.  

3. Dimensionality Reduction (NMF)  
   - Apply NMF with different values of `k` (number of components).  
   - Evaluate cluster stability using CCC.  

4. Consensus Clustering 
   - Perform multiple runs of NMF for each `k`.  
   - Compute consensus matrices and assess clustering consistency.  

5. Model Selection 
   - Plot CCC values across different `k`.  
   - Identify the optimal number of clusters (`best_k`).  

6. Classification with SVM 
   - Train SVM on reduced features (`H` matrix from NMF).  
   - Evaluate model performance using accuracy score.  

