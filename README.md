# Code Documentation Generator

## Introduction
* The Code Documentation Generator is a powerful tool designed to automatically generate comprehensive and well-structured documentation for your code snippets. With just a simple API call, you can get detailed documentation for your code, making it easier to share, understand, and maintain your projects.

## How to Use
* Using the Code Documentation Generator is straightforward. Simply make an API call to the provided endpoint with your code snippet as the input, and you will receive the generated documentation in response.

## API Endpoint
* Make a POST request to the following API endpoint:

   POST https://code-documentation-generator.adarshkumar35.repl.co/api/generate


## Request Body
* The API expects the code snippet to be included in the request body. You can send the code as plain text or as a code file.

## Example using <code>curl</code>
* Here's an example using `curl` to make a request:
```sh
curl -X POST -H "Content-Type: text/plain" -d '
def add(a, b):
    return a + b
' https://code-documentation-generator.adarshkumar35.repl.co/api/generate
```

```sh
curl -X POST -H "Content-Type: text/plain" --data-binary "@path/to/file.txt" https://code-documentation-generator.adarshkumar35.repl.co/api/generate
```

Reading the code from a file and making a request in python
```py
import requests

filename = "" # Path to the source code
with open(filename, 'r') as file:
    code = file.read()

r = requests.post(
    url = "https://code-documentation-generator.adarshkumar35.repl.co/api/generate",
    data = {
        "code": code
    }
)
```

# save the documentation in doc.md
```python
doc = r.text["markdown"]
with open('doc.md', 'w') as file:
    file.write(doc)
```


## Response
* Upon successful processing, you will receive the generated documentation in the response. The documentation will be in Markdown format and will contain sections such as introduction, code structure, dependencies, code explanation, and conclusion.

## Supported Languages
The Code Documentation Generator currently supports a wide range of programming languages, including:
- JavaScript
- Python
- Java
- C++
- C#
- Ruby
- PHP
- Swift
- Go
- TypeScript

# Use Cases
* The Code Documentation Generator is beneficial for developers, teams, and organizations looking to streamline their code documentation process. It can be integrated into development workflows, continuous integration pipelines, and documentation generation systems.

## Get Started
* Start using the Code Documentation Generator today and simplify your code documentation process. Improve code collaboration, understanding, and maintainability with automatically generated, well-structured documentation.

### For any inquiries or questions, please contact <a href="mailto:adarshkumar20012704@gmail.com" target="_new">Adarsh Kumar</a>. We value your feedback and are open to suggestions for further improvements.