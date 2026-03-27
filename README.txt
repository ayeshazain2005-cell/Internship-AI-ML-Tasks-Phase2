AI/ML Engineering Internship - Advanced Tasks
Organization: DevelopersHub 
CorporationIntern: Ayesha
Semester: 6th, BS(CS) - COMSATS University Islamabad


Overview:
This repository contains the completion of the Advanced Task Set, focusing on state-of-the-art AI/ML methodologies including Transformers, Multimodal Learning, Production-Ready Pipelines, and Retrieval-Augmented Generation (RAG).
Task 1: News Topic Classifier Using BERT
ObjectiveFine-tune a bert-base-uncased transformer model to classify news headlines into four categories: World, Sports, Business, and Sci/Tech.
MethodologyPreprocessing: Tokenized the AG News dataset using the BertTokenizer with a max sequence length of 128.
Model: Implemented Transfer Learning by adding a classification head to the pre-trained BERT model.
Training: Utilized the Hugging Face Trainer API with an optimized learning rate of $2e-5$ and weight decay.
Deployment: Integrated a live interaction interface using Gradio.
Key ResultsMetrics: Achieved high Accuracy and Weighted F1-score on the test subset.
Insight: BERT’s attention mechanism significantly outperforms traditional RNNs in understanding the context of short headlines.

Task 2: End-to-End ML Pipeline (Telco Churn)
ObjectiveBuild a reusable, production-ready pipeline to predict customer churn using the Telco Churn dataset.
MethodologyPipeline API: Used sklearn.pipeline to combine StandardScaler for numeric features and OneHotEncoder for categorical data.
Models: Evaluated Logistic Regression and Random Forest.Optimization: Conducted GridSearchCV to tune hyperparameters (n_estimators, max_depth).
Persistence: Exported the final trained model as a .joblib file for instant reusability in production.
Key ResultsEfficiency: The pipeline ensures that data leakage is prevented by applying transformations consistently during cross-validation.
Model Choice: Random Forest provided the best balance between precision and recall for churn detection.

Task 3: Multimodal ML – Housing Price Prediction
ObjectivePredict housing prices by fusing two distinct data modalities: architectural house images and structured tabular data.
MethodologyVisual Branch: Developed a CNN to extract high-level spatial features from house images.
Tabular Branch: A Multi-Layer Perceptron (MLP) processed numerical house features.
Late Fusion: Combined features from both branches using a concatenation layer (torch.cat) followed by final regression layers.
Evaluation: Measured performance using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).
Key ResultsObservation: The multimodal approach captures nuances (like "curb appeal" from images) that tabular data alone cannot represent.

Task 4: Context-Aware Chatbot (RAG)
ObjectiveDevelop a conversational AI capable of retrieving information from a custom knowledge base while maintaining chat history.
MethodologyFramework: Built using LangChain and OpenAI/HuggingFace LLMs.
RAG Pipeline: Documents were split into chunks, embedded using vector embeddings, and stored in a vector database.
Memory: Integrated ConversationBufferMemory to allow the bot to remember previous user inputs.
Deployment: Hosted on Streamlit for a clean, user-friendly chat interface.
Key ResultsPerformance: Successfully reduced "hallucinations" by grounding the LLM's responses in provided documents.

Tech StackDeep Learning: PyTorch, TensorFlow, CNNsNLP: Hugging Face Transformers (BERT), LangChainML Ops: Scikit-learn Pipeline, JoblibDeployment: Gradio, StreamlitData Science: Pandas, NumPy, Matplotlib