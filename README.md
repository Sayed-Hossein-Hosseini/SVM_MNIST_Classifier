# 🖋️ SVM-MNIST-Classifier 🚀

A **Support Vector Machine (SVM)** based handwritten digit classifier trained on the popular **MNIST dataset** 🖼️ ➡️ 🔢.

This project demonstrates how to implement a multi-class SVM classifier using:
- The **dual form of SVM** optimization problem
- **cvxopt** quadratic programming solver
- **Batch-based training** to handle large-scale data
- **One-vs-Rest (OvR)** strategy for multi-class classification
- Visualization of model performance via **confusion matrix**

---

## 📌 Project Highlights

✅ From-scratch implementation of SVM using `cvxopt`  
✅ Supports **batch training** to overcome memory limitations  
✅ Clear step-by-step code structure for educational purposes  
✅ Easy to adapt to other datasets  
✅ Clean visualization of results  

---

## 🎥 Demo

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/2/27/MnistExamples.png" width="300" alt="MNIST Digits">
</p>


## 🚀 Installation

1️⃣ Clone the repository:

```bash
git clone https://github.com/your-username/svm-mnist-classifier.git
cd svm-mnist-classifier
````

2️⃣ Create a virtual environment (optional but recommended):

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3️⃣ Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 📝 Usage

Run the main training script:

```bash
python main.py
```

Or use the included **Jupyter Notebook** for an interactive experience:

```bash
jupyter notebook SVM_MNIST_Batch_Training.ipynb
```

---

## ⚙️ Project Structure

```
svm-mnist-classifier/
├── data/                     # optional data folder
├── SVM_MNIST_Batch_Training.ipynb  # optional interactive notebook
└── README.md                 # this file
```

---

## 🧠 Methodology

### Multi-Class SVM

Since MNIST contains 10 classes (digits 0–9), a **One-vs-Rest** approach is used:

* Train 10 binary SVM classifiers.
* Each classifier predicts whether an input is its corresponding digit.
* At inference, the classifier with the highest score is selected.

### Batch Training

To handle the large MNIST training set (\~60,000 images), we train SVMs on **batches** of data to avoid memory issues when solving the dual problem with `cvxopt`.

---

## 🏆 Results

| Metric        | Value                                 |
| ------------- | ------------------------------------- |
| Test Accuracy | \~78.68% (depends on batch size & C)  |

---

## 📚 Dependencies

* `numpy`
* `matplotlib`
* `keras`
* `cvxopt`
* `scikit-learn` (for confusion matrix)
* 
---

## 🚀 Possible Improvements

* Implement **non-linear kernels** (RBF, polynomial)
* Perform **hyperparameter tuning** on C and kernel params
* Use **ensemble of batch models** for improved accuracy
* Implement **parallel training** for faster performance
* Add **automatic evaluation metrics** (Precision, Recall, F1)

---

## 📖 References

* [MNIST Dataset](http://yann.lecun.com/exdb/mnist/)
* [Support Vector Machines Explained](https://cs231n.github.io/linear-classify/#svm)
* [cvxopt documentation](https://cvxopt.org/)

---

## 📜 License

MIT License
Feel free to use, modify, and share ⭐

---

## ❤️ Acknowledgements

This project was built for **educational purposes**, demonstrating how to build an SVM classifier from scratch on a large dataset.
Inspired by classic ML courses and hands-on experience.

* Student: **Sayyed Hossein Hosseini DolatAbadi**

---

**If you like this project, please ⭐️ the repo and share it!**
Pull requests are welcome 🚀
