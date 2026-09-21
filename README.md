# ML_LEAP-Final-Project
CNN Image Classification for using TensorFlow and KERAS.

Project Overview :

This project trains and compares two Convolutional Neural Networks (CNNs) to read handwritten digits using the MNIST dataset. The primary goal is to evaluate a baseline model, identify its common classification errors, and attempt to fix those mistakes by modifying the neural network architecture. Both models utilize the exact same training configuration, including early stopping rules, to ensure a completely fair comparison.

Data, Method, and Model Workflow :

The project uses standard grayscale handwritten digit images. Preprocessing involves normalizing pixel values to scale inputs appropriately for neural network training. The workflow consists of two iterations: a baseline CNN trained over fifteen epochs, and a deeper CNN that incorporates a second convolutional block aimed at extracting finer visual patterns. Evaluation is conducted by inspecting test accuracy, loss curves, and detailed confusion matrices to map out misclassification patterns.

Results and Comparison :

The baseline model achieved a 98.64% test accuracy over fifteen epochs. However, it frequently confused visually similar digits, mistaking the number 4 for a 9 twenty-four times, and a 2 for an 8 ten times. The second, deeper model was designed to fix these specific errors, but its overall accuracy dropped slightly to 98.12%. Analyzing the confusion matrices showed that while structural changes altered some error patterns, the deeper network did not achieve the expected general performance boost.

Reflection and Challenges :

The most difficult challenge in this project was understanding why adding depth to the network led to worse performance instead of better results. Initially, it was surprising that a deeper architecture designed to capture more complex features performed below the shallow baseline. The key insight came from reviewing the training logs under the fixed experimental setup. Because both models used the exact same early stopping rule, the deeper network triggered early stopping after just three epochs. The increased parameter count required more time to optimize, meaning the rule halted training prematurely before the deeper model could fully converge. In future work, early stopping patience should be scaled relative to model complexity rather than held rigid across different architectures.

Ethical Risks :

Real-world deployment of handwritten digit recognition systems carries notable ethical risks because handwriting varies heavily by age, education, physical ability, and region. Standard training datasets often under-represent children, elderly individuals, and international populations with distinct script styles. If a model makes confident but incorrect predictions on these marginalized groups, it can cause severe downstream harms, such as misrouting essential mail or causing financial errors in automated banking systems.

How to Run the Project
To run this notebook, ensure you have TensorFlow, Keras, NumPy, Matplotlib, and Jupyter installed on your machine. Launch Jupyter Notebook from your terminal, open the project file, and run all cells sequentially from top to bottom. Once execution finishes, all training logs, confusion matrices, and figures will be visible directly within the notebook.
