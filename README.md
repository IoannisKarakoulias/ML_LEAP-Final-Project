# ML_LEAP-Final-Project
CNN Image Classification for using TensorFlow and KERAS.

Project Overview :

This project trains and compares two Convolutional Neural Networks to read handwritten digits. The goal is to evaluate a baseline model, identify its common mistakes, and attempt to fix them by modifying the model's architecture. Both models use the exact same training settings, including early stopping, to ensure a fair comparison.

Results and Comparison :

The first model achieved 98.64% accuracy over fifteen epochs, but frequently confused visually similar digits, mistaking 4 for 9 twenty-four times and 2 for 8 ten times. I predicted that adding a second convolutional block would fix this. However, the second model's accuracy dropped slightly to 98.12%. This happened because the early stopping rule halted its training after just three epochs. Due to this shortened training time, the deeper network could not fully converge, failing to provide the expected performance boost.

Ethical Risks : 

Real-world deployment of this model carries risks because handwriting varies heavily by age, education, and region. Standard datasets often under-represent children, the elderly, and international populations. If the model makes a confident but incorrect prediction for these groups, it could cause serious harms like misrouting mail or creating financial errors.

How to Run the Project :

To run this notebook, ensure you have TensorFlow, NumPy, Matplotlib, and Jupyter installed on your machine. Launch Jupyter Notebook from your terminal, open the downloaded file, and run all cells sequentially from top to bottom. Once finished, you will be able to view the confusion matrices and the final written analysis directly in the notebook.
