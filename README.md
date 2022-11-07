# AylaDocs
This is a documentation intended to give instructions and better explain how Ayla works.

## 📚 Table of Contents
   - [PyApi](#🎃-pyapi)

## 🎃 PyAPI
Available at [Hospital-Screening repo](https://github.com/ayla-tcc/Hospital-screening)
### Requirements

- Python 3.8 or higher
- pip
- git
```bash
pip install -r requirements.txt
# Available at this repository
```
### Running
```bash
# Frist Clone the repository
git clone https://github.com/ayla-tcc/Hospital-screening.git
# Then go to the folder
cd ./pyApi
# Run the server
python -m uvicorn main:app --reload --host 0.0.0.0 --port 8000
```
### Testing
1. Go to [Localhost](http://127.0.0.1:8000/docs)