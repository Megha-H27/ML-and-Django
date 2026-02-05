## Radiation Classification System using Support Vector Machine (SVM)

This Django-based web application classifies atmospheric radiation into *Gamma (Signal)* or *Hadron (Background). It utilizes a Support Vector Machine (SVM) model to find the optimal hyperplane that separates the two particle classes based on Cherenkov telescope data.

![WhatsApp Image 2026-02-05 at 3 36 02 PM](https://github.com/user-attachments/assets/dd44d45f-7573-4709-bbfd-82c1a4da0678)
![WhatsApp Image 2026-02-05 at 3 36 03 PM](https://github.com/user-attachments/assets/da155bae-c922-4268-82c0-331da9a5aa95)

![WhatsApp Image 2026-02-05 at 3 40 36 PM](https://github.com/user-attachments/assets/acf25349-0de4-4b09-b0d6-c42bbebfa2a1)


## 🧠 Machine Learning: Support Vector Machine
The core of this project is an SVM classifier. SVM was chosen for its effectiveness in high-dimensional spaces and its ability to create a clear margin of separation between the complex features of Gamma and Hadron showers.



### Model Integration
The model is integrated directly into the Django backend:
- *Persistence:* The trained SVM model is loaded via joblib or pickle inside views.py.
- *Inference:* User inputs from the frontend are processed as a feature vector and passed to model.predict().
- *Persistence:* Results are stored in the database linked to the SVM prediction output.

## 🚀 Features
- *SVM Prediction Engine:* High-accuracy classification using a radial basis function (RBF) or linear kernel.
- *Django Integration:* A seamless bridge between the Python ML logic and the web interface.
- *Database Tracking:* Every prediction is logged with its input parameters for further data analysis.

## 🛠️ Technical Implementation
### Views.py Logic
In your views.py, the flow operates as follows:
1. Capture POST data from the input form.
2. Scale the data (if a scaler was used during training).
3. Run the SVM model: prediction = svm_model.predict(input_features).
4. Save the instance to the database: ClassificationResult.objects.create(...).
5. Return the result to the template.

*Developed for high-energy physics data analysis.*
## 📂Project Structure

<img width="524" height="932" alt="Screenshot 2026-02-05 214133" src="https://github.com/user-attachments/assets/71c45ed3-3e24-468e-8a31-c16d3a4677cf" />
<img width="449" height="132" alt="Screenshot 2026-02-05 214146" src="https://github.com/user-attachments/assets/eed950e1-12f8-408b-9d98-2c06a334c926" />


