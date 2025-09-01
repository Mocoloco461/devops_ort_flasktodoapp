FROM python:3.8.3-slim-buster

# שדרוג pip
RUN python -m pip install --upgrade pip

# העתק requirements.txt קודם (כדי לאפשר caching)
WORKDIR /app
COPY requirements.txt .

# התקנת חבילות
RUN pip install -r requirements.txt

# העתקת הקבצים (ללא requirements.txt שכבר הועתק)
COPY testserver.py .

# פקודת ברירת מחדל
CMD ["python", "testserver.py"]