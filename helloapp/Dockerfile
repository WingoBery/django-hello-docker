# 1. Base image
FROM python:3.10-slim

# 2. Working directory
WORKDIR /app

# 3. Copy project files
COPY . .

# 4. Install dependencies
RUN pip install --no-cache-dir django gunicorn

# 5. Expose port
EXPOSE 8000

# 6. Start server using gunicorn
CMD ["gunicorn", "hello_project.wsgi:application", "--bind", "0.0.0.0:8000"]
