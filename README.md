# Azure Function: PDF Generator

This Azure Function generates **PDF files** from JSON input. Users can send data like invoice or report details and receive a PDF.

## Features

- Input JSON data via HTTP POST request.
- Generates a PDF using ReportLab library.
- Returns PDF as response.

## Setup (Windows)

1. **Install Python** (if not installed): https://www.python.org/downloads/

2. **Install Azure Functions Core Tools**:
   ```powershell
    npm i -g azure-functions-core-tools@4 --unsafe-perm true
   ```

3. **Clone repository**:
```powershell
    git clone https://github.com/alvenkatesh100/Pdf_generator.git
    cd azure-function-pdf
```

4. **Create virtual environment**:
```powershell
    python -m venv venv
    .\venv\Scripts\activate
```

5. **Install dependencies**:
```powershell
    pip install -r requirements.txt
```

6. **Run locally**:
```powershell
    func start
```

6. **Test API**:
```powershell
    POST http://localhost:7071/api/PdfGeneratorFunction
    JSON body:
    {
        "title": "Invoice",
        "name": "John Doe",
        "amount": "$100"
    }

```
