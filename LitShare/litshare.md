# LitShare (2025-2026 Capstone Project)

LitShare is a social book-sharing platform that empowers readers to organize their personal libraries, create curated booklists, and discover their next favourite read through personalized recommendations. By bridging the gap between social networking and literary discovery, it transforms the reading experience into a collaborative community journey. 

<img width="2000" height="1500" alt="image" src="https://github.com/user-attachments/assets/9c9206de-d6b6-43db-8b05-931143b2b258" />

The platform is powered by a Bayesian recommendation model which leverages both book description embeddings (currently 512-dim vectors obtained from book synopses using RoBERTa-XLM) as well as collaborative signals to deliver timely and relevant recommendations for each LitShare user. The candidate pool is generated using cosine similarity as well as user-specified filters such as keyword search, authors, publication year, number of pages, etc.

Mustafa Abdulameer is largely responsible for the ML component of the project, including design of model architecture, training, and evaluation. The model is trained with a 64-dim latent vector (both users and books are feature projected into a latent space). The ensemble model uses Bayesian Model Averaging - predictions from the submodels (currently ten) are weighted by posterior probability in order to provide more robust results.

Book Feature Vector:

![alt text](featvec.png)

Here is a video demonstration of the "infinite scroll" explore page which is connected to the model.

[![Watch the video](https://img.youtube.com/vi/whWrx5M9duM-C0/0.jpg)](https://www.youtube.com/watch?v=whWrx5M9duM-C0)

Current Explore Page:

<img width="1694" height="1227" alt="image" src="https://github.com/user-attachments/assets/120981fa-6d02-4216-befe-f0c9f52500f0" />

