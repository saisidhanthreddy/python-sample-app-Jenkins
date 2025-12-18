# Sample Python Application for Jenkins CI

This is a simple Python calculator application designed to demonstrate Continuous Integration (CI) with Jenkins.

## Project Structure

```
sample-python-application/
├── calculator.py          # Main calculator application
├── test_calculator.py     # Unit tests
├── requirements.txt       # Python dependencies
├── Dockerfile            # Docker container configuration
├── .dockerignore         # Files to exclude from Docker build
├── Jenkinsfile           # Jenkins CI/CD pipeline configuration
└── README.md             # This file
```

## Features

- Simple calculator with basic arithmetic operations (add, subtract, multiply, divide, power)
- Comprehensive unit tests using pytest
- Jenkins pipeline configuration for automated testing

## Prerequisites

- Python 3.7 or higher
- pip (Python package installer)
- Docker (optional, for containerized deployment)
- Jenkins (for CI/CD)

## Local Setup

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the application:
```bash
python calculator.py
```

3. Run tests:
```bash
pytest test_calculator.py -v
```

4. Run tests with coverage:
```bash
pytest test_calculator.py --cov=calculator --cov-report=term-missing
```

## Docker Setup

### Build Docker Image

```bash
docker build -t calculator-app .
```

### Run Docker Container

```bash
# Run the application
docker run --rm calculator-app

# Run tests inside container
docker run --rm calculator-app pytest test_calculator.py -v

# Run tests with coverage
docker run --rm calculator-app pytest test_calculator.py --cov=calculator --cov-report=term-missing
```

### Interactive Shell

```bash
docker run -it --rm calculator-app /bin/bash
```

## Jenkins CI Setup

1. **Create a new Jenkins Pipeline job:**
   - Go to Jenkins Dashboard
   - Click "New Item"
   - Enter a job name
   - Select "Pipeline" and click OK

2. **Configure the Pipeline:**
   - In Pipeline configuration, select "Pipeline script from SCM"
   - Choose your SCM (Git, SVN, etc.)
   - Enter your repository URL
   - Set Script Path to `Jenkinsfile`

3. **Pipeline Stages:**
   - **Checkout**: Checks out source code from repository
   - **Setup Python Environment**: Verifies Python installation
   - **Install Dependencies**: Installs required Python packages
   - **Lint**: Runs code linting with flake8
   - **Test**: Runs unit tests with pytest
   - **Test with Coverage**: Generates test coverage report

4. **Run the Pipeline:**
   - Click "Build Now" to trigger the pipeline
   - View progress in the build console output

## Testing

The application includes comprehensive unit tests covering:
- All arithmetic operations
- Edge cases (zero, negative numbers)
- Error handling (division by zero)

## License

This is a sample application for educational purposes.
thsi
