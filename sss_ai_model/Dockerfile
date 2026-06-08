FROM python:3.10-slim

WORKDIR /app

# تسطيب مكتبات النظام الضرورية لـ OpenCV و Pillow
RUN apt-get update && apt-get install -y \
    libglib2.0-0 \
    libgl1 \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

ENV PORT=8080
EXPOSE 8080

# تأكدي إن الملف اسمه app1.py وموجود جوه فولدر sss_ai_model
CMD ["uvicorn", "app1:app", "--host", "0.0.0.0", "--port", "8080"]    
