# **Quantum Quest: Exploring Quantum Randomness and Algorithms**

**Quantum Quest** is a cutting-edge project that explores the fascinating world of quantum computing by implementing a Quantum Random Number Generator (QRNG) and optimizing classical algorithms with Grover's and Shor's quantum algorithms. This project integrates various quantum computing concepts using **Qiskit** (for quantum programming), **ReactJS** (for the frontend dashboard), and **Flask** (for backend integration). The project also compares quantum-generated randomness with classical pseudo-random number generation, validating its accuracy and performance.

## **Table of Contents**

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Algorithms Implemented](#algorithms-implemented)
  - [Quantum Random Number Generator (QRNG)](#quantum-random-number-generator-qrng)
  - [Grover’s Algorithm](#grovers-algorithm)
  - [Shor’s Algorithm](#shors-algorithm)
- [Benchmarking and Comparison](#benchmarking-and-comparison)
- [Frontend: React Dashboard](#frontend-react-dashboard)
- [Backend: Flask API](#backend-flask-api)
- [Testing](#testing)
- [Contributing](#contributing)
<!-- - [License](#license)-->
- [Acknowledgements](#acknowledgements)

## **Project Overview**

**Quantum Quest** aims to bring quantum computing into the realm of practical applications by building a high-performance Quantum Random Number Generator (QRNG). By leveraging the power of quantum superposition and entanglement, this project demonstrates the superior randomness of quantum-generated numbers compared to classical pseudo-random number generators (PRNG). Additionally, Grover’s and Shor’s algorithms are implemented to showcase how quantum algorithms can optimize unstructured search queries and factorize integers efficiently.

## **Features**

- **Quantum Random Number Generator (QRNG):** Generates random numbers using quantum circuits, achieving up to 94.7% randomness validation accuracy.
- **Grover's Algorithm:** Optimizes unstructured search queries using quantum parallelism.
- **Shor's Algorithm:** Performs integer factorization, demonstrating the power of quantum computing in cryptography.
- **React Dashboard:** A user-friendly interface for visualizing quantum randomness and algorithm executions.
- **Benchmarking:** Performance comparison of quantum and classical PRNGs, along with their accuracy validation.
- **Full-stack Integration:** Flask backend to serve quantum data to the ReactJS frontend, enabling a seamless user experience.

## **Technologies Used**

- **Qiskit:** Open-source quantum computing framework for creating and running quantum algorithms.
- **ReactJS:** Frontend JavaScript library for building the user dashboard.
- **Flask:** Python web framework for backend API integration.
- **Jupyter Notebook:** For prototyping and experimenting with quantum circuits and algorithms.
- **Python:** Programming language used to implement quantum algorithms and backend logic.
- **NumPy, Matplotlib:** For numerical operations and visualizing results.
- **Heroku/Vercel/Netlify:** Deployment platforms for the backend and frontend.

## **Installation**

### **1. Clone the repository**
```bash
git clone https://github.com/your-username/quantum-quest.git
cd quantum-quest
```

### **2. Install Python dependencies**
Create and activate a virtual environment, then install the required Python libraries:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
pip install -r requirements.txt
```

### **3. Set up ReactJS frontend**
Navigate to the `quantum-dashboard` directory and install the required dependencies:
```bash
cd quantum-dashboard
npm install
```

### **4. Run the Backend**
Start the Flask API server:
```bash
cd backend
python app.py
```

### **5. Run the Frontend**
Start the ReactJS development server:
```bash
cd quantum-dashboard
npm start
```

## **Usage**

Once both the backend and frontend are running, navigate to `http://localhost:3000` to access the **Quantum Quest** dashboard. The dashboard will allow you to:

- View quantum-generated random numbers in real-time.
- Compare quantum randomness with classical PRNGs.
- Visualize the results of Grover’s and Shor’s algorithms.

## **Algorithms Implemented**

### **Quantum Random Number Generator (QRNG)**
Quantum random numbers are generated using quantum circuits in Qiskit. The `Hadamard` gate is applied to all qubits to achieve superposition, and then a measurement is made to generate random bits. This randomness is validated by calculating entropy, ensuring the numbers are close to truly random.

### **Grover’s Algorithm**
Grover’s algorithm is implemented to perform a search optimization in an unsorted database. It uses quantum parallelism to search for a marked item with fewer queries than classical algorithms. This implementation uses Qiskit’s quantum gates to build the circuit and simulate the search process.

### **Shor’s Algorithm**
Shor's algorithm is implemented to factorize large integers, a task that is exponentially faster on a quantum computer compared to classical methods. This implementation uses Qiskit’s built-in Shor algorithm to find the prime factors of numbers efficiently.

## **Benchmarking and Comparison**

The performance and accuracy of the **Quantum Random Number Generator (QRNG)** are benchmarked against classical **Pseudo Random Number Generators (PRNG)**. The quantum RNG is validated for randomness using entropy calculations and compared with classical RNGs using Python’s `random` module.

### **Randomness Validation Accuracy**
- **Quantum RNG:** Achieves 94.7% randomness validation accuracy.
- **Classical PRNG:** Benchmark data from Python’s `random` module is used for comparison.

## **Frontend: React Dashboard**

The ReactJS frontend is a dynamic dashboard that visualizes the quantum-generated random numbers and algorithm results. Key features include:

- **Real-time Display:** Shows the latest random numbers generated by the quantum circuit.
- **Interactive Visualization:** Visualizes quantum algorithm executions, including Grover’s and Shor’s results.
- **Performance Graphs:** Displays benchmarking results comparing quantum and classical PRNGs.

### **Components:**
- **QRNG Visualization:** Real-time generation of quantum random numbers.
- **Grover’s Search Visualization:** Step-by-step display of Grover’s algorithm process.
- **Shor’s Algorithm Visualization:** Prime factorization process using Shor’s algorithm.

## **Backend: Flask API**

The backend is built with Flask to handle requests between the frontend and the quantum simulations. Key endpoints include:

- `/api/random-number`: Returns quantum-generated random numbers.
- `/api/benchmark`: Provides benchmarking data comparing quantum vs classical PRNGs.
- `/api/grover`: Runs Grover’s algorithm and returns the results.
- `/api/shor`: Runs Shor’s algorithm and returns the factorization results.

## **Testing**

Unit tests are written for both the quantum algorithm implementations and the Flask API endpoints. Frontend testing is done using React Testing Library and Jest to ensure that all components are working as expected.

To run tests:
```bash
# Run backend tests
python -m unittest discover backend/tests

# Run frontend tests
npm test
```

## **Contributing**

We welcome contributions! If you have any ideas or improvements, feel free to fork the repository and submit a pull request. Please ensure that your changes are well-tested and documented.
<!--
## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
-->
## **Acknowledgements**

- **Qiskit:** The open-source quantum computing framework that powers the QRNG and quantum algorithms.
- **ReactJS:** The JavaScript library for building the frontend dashboard.
- **Flask:** A micro web framework used for backend API development.
- **Matplotlib & NumPy:** For data visualization and numerical operations.
- **IBM Q Experience:** For providing access to real quantum computers.
