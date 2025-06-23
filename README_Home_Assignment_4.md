# Home Assignment 4 – CS5720 Neural Networks and Deep Learning

**Student Name:** Vaishnavi Gopi  
**Course:** CS5720 – Neural Networks and Deep Learning  
**University:** University of Central Missouri  
**Semester:** Summer 2025  

---


## ✅ Contents

### 1. GAN Architecture (Theory)
- **Goal of Generator:** Generate data indistinguishable from real data.
- **Goal of Discriminator:** Distinguish between real and generated data.
- They improve through a **min-max game**, where:
  - Generator tries to fool the discriminator.
  - Discriminator gets better at detecting fakes.

        +--------------------+         +--------------------+
        |    Random Noise    |         |     Real Data      |
        |       Vector z     |         |    (e.g., MNIST)   |
        +---------+----------+         +----------+---------+
                  |                              |
             +----v----+                    +----v----+
             | Generator|                    |         |
             |   G(z)   |                    |         |
             +----+----+                    |         |
                  |                         |         |
        +---------v----------+      +-------v---------+
        |   Generated Image   |     |   Real Image     |
        +---------+----------+      +--------+--------+
                  |                         |
                  +-----------+-------------+
                              |
                         +----v----+
                         |Discriminator|
                         |     D(x)     |
                         +----+----+
                              |
                    Predicts Real (1) or Fake (0)


### 2. Ethics and AI Harm

**Harm Selected:** Misinformation in Generative AI  
**Example:** AI-generated fake news articles during elections.  
**Mitigation Strategies:**
1. Include watermarking in generated content.
2. Add fact-checking layers in deployment pipelines.

---

### 3. Programming Task – Basic GAN (PyTorch)

- Implemented a basic GAN to generate handwritten digits using MNIST.
- Includes:
  - Generator and Discriminator architectures
  - Training loop with loss plots
  - Epoch 0, 50, and 100 sample generations

📂 Code: `gan_mnist_colab.ipynb`  
📸 Sample images & loss plots are embedded in the notebook.

---

### 4. Programming Task – Data Poisoning on Sentiment Classifier

- A simple sentiment classifier was trained on a movie review dataset.
- Labels about "UC Berkeley" were flipped in poisoned data.
- Impact:
  - Accuracy decreased significantly.
  - Confusion matrix shifted with increased misclassifications.

📂 Code: `data_poisoning_simulation.ipynb`  
📈 Includes before/after graphs.

---

### 5. Legal and Ethical Implications of GenAI

- **Concerns:**
  - Models memorizing private data (e.g., names in GPT-2)
  - Generating copyrighted material (e.g., Harry Potter)
- **Opinion:** Yes, GenAI models should be restricted from such data to avoid IP/legal violations and protect privacy.

---

### 6. Bias & Fairness Tools – Aequitas

**Metric Chosen:** False Negative Rate Parity  
- **Measures:** If FNR is equal across demographic groups.
- **Importance:** Prevents unfair denial of benefits (e.g., loans).
- **Failure Scenario:** One group may get unfairly high rejection rates.

🔗 Tool: https://www.datasciencepublicpolicy.org/our-work/aequitas/

---

## 🎥 Submission Checklist

- [x] GitHub repo with code and README ✅
- [x] Video (2–3 min) showing code and explanation ✅
- [x] Code is commented and clean ✅

---

