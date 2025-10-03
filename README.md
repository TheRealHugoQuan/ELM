
----Project is currently under revision----

📘 Extreme Learning Machine (ELM)
🚀 Overview

This project implements an Extreme Learning Machine (ELM) — a type of single hidden layer feedforward neural network (SLFN) known for its fast training speed and good generalization performance. Unlike traditional backpropagation-based networks, ELM randomly assigns input weights and biases, then analytically determines output weights using a closed-form solution (typically least squares).

ELM is especially useful for:

Real-time signal classification

Portable embedded systems (FPGA/MCU deployment)

Scenarios where low-latency and efficiency matter more than massive model complexity

⚙️ Features

✅ Single hidden layer neural network with random hidden weights

✅ Closed-form solution for output weights (Moore–Penrose pseudoinverse / regularized least squares)

✅ Configurable activation functions (sigmoid, tanh, ReLU, custom)

✅ Lightweight implementation for embedded and FPGA acceleration

✅ Example datasets and test scripts included

📂 Project Structure
ELM/
│── data/              # Example datasets
│── src/               # Core ELM implementation
│   ├── elm_train.py   # Training function
│   ├── elm_test.py    # Evaluation function
│   ├── activation.py  # Supported activation functions
│── examples/          # Example usage scripts
│── docs/              # Documentation and references
│── README.md          # Project documentation (this file)

🧑‍💻 Installation

Clone this repo:

git clone https://github.com/your-username/ELM.git
cd ELM


(Optional) Create and activate a Python virtual environment:

python3 -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows


Install dependencies:

pip install -r requirements.txt

▶️ Usage
Training
python src/elm_train.py --data data/mnist.npz --hidden 1000 --activation sigmoid

Testing
python src/elm_test.py --data data/mnist.npz --model saved/elm_model.pkl

📊 Example Results

Dataset: MNIST (10 classes, 60k samples)

Hidden neurons: 1000

Accuracy: ~95% in under 5 seconds of training on CPU

🔧 Configuration

Key parameters:

--hidden : number of hidden neurons

--activation : activation function (sigmoid, tanh, relu)

--regularization : regularization factor (for numerical stability)

📘 References

Huang, G. B., Zhu, Q. Y., & Siew, C. K. (2006). Extreme learning machine: Theory and applications. Neurocomputing, 70(1-3), 489–501.

Official ELM Website: https://www.ntu.edu.sg/home/egbhuang/elmRandom.html

🤝 Contributing

Pull requests are welcome! If you’d like to contribute:

Fork the project

Create your feature branch (git checkout -b feature/new-feature)

Commit your changes (git commit -m "Add new feature")

Push to the branch (git push origin feature/new-feature)

Open a pull request

📜 License

This project is licensed under the MIT License — see the LICENSE
 file for details.
