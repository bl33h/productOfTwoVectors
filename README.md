# productOfTwoVectors
This code leverages CUDA to perform parallel element-wise multiplication of two vectors using a GPU. It allocates memory for the input and output vectors, initializes the input vectors, and transfers the data to the GPU. The CUDA kernel function executes the multiplication in parallel and displays intermediate results. Finally, the code copies the result back to the host, verifies it, frees the memory, and terminates. It showcases how CUDA harnesses GPU parallelism to accelerate vector operations effectively.

<p align="center">
  <br>
  <img src="https://upload.wikimedia.org/wikipedia/commons/b/bc/Cross_product_parallelogram.gif?20191208165026" alt="pic" width="500">
  <br>
</p>
<p align="center" >
  <a href="#Files">Files</a> •
  <a href="#Features">Features</a> •
  <a href="#how-to-use">How To Use</a> 
</p>

## Files

- src: the file that implements de solution.

## Features
The main features of the application include:
- Parallel Processing: It utilizes CUDA to execute the `productOfTwoVectors` kernel function in parallel on a GPU. This allows for efficient processing of the element-wise vector multiplication by utilizing multiple threads.
- Memory Management: The code demonstrates proper memory allocation and deallocation for both host and device memory. It uses `cudaMalloc()` to allocate memory on the GPU and `free()` to free the memory on the host.
- Data Transfer: The code utilizes `cudaMemcpy()` to transfer data between the host and the device. It copies the input vectors from the host memory to the device memory and copies the result vector from the device memory back to the host memory.
- Error Handling: The code checks for errors after each CUDA operation and prints error messages if any occur. It ensures proper error handling and termination of the program in case of failures.
- Verification: After the computation, the code verifies the correctness of the result vector by comparing it with the sum of the individual elements. It checks for any discrepancies and displays an error message if the verification fails.
- Intermediate Result Display: The code prints intermediate results during the execution of the `productOfTwoVectors` kernel function. It displays the multiplication of each pair of elements from the input vectors, providing insight into the parallel computation process.

## How To Use
To clone and run this application, you'll need [Git](https://git-scm.com) and a [C++ compiler](https://www.fdi.ucm.es/profesor/luis/fp/devtools/mingw.html) installed on your computer. From your command line:

```bash
# Clone this repository
$ git clone https://github.com/bl33h/productOfTwoVectors


# Open the folder
$ cd src

# Run the app
$ g++ productOfTwoVectors.cpp -o productOfTwoVectors
$ ./productOfTwoVectors
```

Alternatively, you can run the code using Google Colab:
1. [Open Google Colab](https://colab.research.google.com) in your web browser.
2. Click on "File" in the top menu, then select "Open notebook".
3. In the "GitHub" tab, enter the repository URL: https://github.com/bl33h/productOfTwoVectors
4. Choose the desired notebook file and click "Open".
5. Follow the instructions within the Colab notebook to execute the code.

Note: Running the code in Google Colab requires an internet connection and a Google account. It provides a convenient online environment for executing code without the need for local setup or dependencies.
