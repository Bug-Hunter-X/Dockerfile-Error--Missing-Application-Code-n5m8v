# Dockerfile Bug: Missing Application Code

This repository demonstrates a common error in Dockerfiles: forgetting to copy the application code into the image.

The `Dockerfile` attempts to run a Python application, but the application code is missing.

The `Dockerfile_solution` provides a corrected version that includes the necessary `COPY` command to include application code.

## Steps to reproduce the bug:

1. Clone the repository.
2. Build the image using the `Dockerfile`:
   ```bash
   docker build -t missing-app . 
   ```
3. Try to run the image:
   ```bash
   docker run missing-app
   ```
You will see an error indicating that the python interpreter cannot find the application code. 

## Solution:

The solution involves adding a `COPY` command to copy the application code from the build context to the image.  The `Dockerfile_solution` provides this correction.
