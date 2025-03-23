# My-Docker-Image-Generator

## Overview
My-Docker-Image-Generator is a tool that utilizes AI assistance to automatically generate Dockerfiles, `docker-compose.yml`, and other configuration files based on the project structure. This simplifies the process of containerizing applications.

## Features
- Automatically detects the project framework.
- Generates Dockerfiles for various frameworks including Python, React, Streamlit, Angular, Java, Ruby, C++, and Fullstack applications.
- Generates a `.dockerignore` file to optimize the build process.
- Uses AI to generate `docker-compose.yml` and `dockerreadme.md` for better container orchestration.
- Provides CLI support for easy usage.
- Supports advanced customization for generated files.

## Installation
To install My-Docker-Image-Generator, use:
```sh
pip install .
```

## Usage
To generate Docker configuration files, run:
```sh
python -m my_docker_generator.main [project_directory] [python_variant]
```

### Parameters:
- `project_directory` (Optional): The path to the project directory. Defaults to the current directory.
- `python_variant` (Optional): If the project is Python-based, specify `flask` or `django` to generate an appropriate Dockerfile.

### Example:
For a Flask project:
```sh
python -m my_docker_generator.main /path/to/project flask
```

For a Django project:
```sh
python -m my_docker_generator.main /path/to/project django
```

For a generic project:
```sh
python -m my_docker_generator.main /path/to/project
```

## Project Structure
```
we4techai-my-docker-image-generator/
├── README.md
└── my_docker_generator/
    ├── setup.py
    └── my_docker_generator/
        ├── __init__.py
        ├── ai_utils.py
        ├── docker_generator.py
        ├── file_utils.py
        ├── framework_detector.py
        ├── main.py
        ├── requirements.txt
        ├── config/
        │   ├── default_config.json
        │   ├── custom_templates/
        │   └── settings.py
        └── __pycache__/
```

## Dependencies
The project requires the following dependencies:
- `groq`
- `pydantic`
- `httpx`
- `typing_extensions`
- `certifi`
- `sniffio`
- `distro`
- `anyio`

Dependencies are listed in `requirements.txt`.

## How It Works
1. **Detects Framework**: The tool analyzes the project structure to determine the framework.
2. **Generates Dockerfile**: Based on the detected framework, it creates a `Dockerfile`.
3. **Generates docker-compose.yml**: Uses AI to generate a `docker-compose.yml` file.
4. **Generates .dockerignore**: Creates a `.dockerignore` file to improve build performance.
5. **Generates Documentation**: Generates a `dockerreadme.md` file using AI to document how to use the generated files.
6. **Supports Customization**: Allows users to modify and fine-tune generated configurations.

## Supported Frameworks
- Python (Flask, Django, Generic)
- React
- Streamlit
- Angular
- Java
- Ruby
- C++
- Fullstack (Python + React)

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch.
3. Make your changes and commit them.
4. Submit a pull request.

## License
This project is licensed under the MIT License.

