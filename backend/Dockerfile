FROM python:3.13-slim
ENV PYTHONDONTWRITEBYTECODE=1 PYTHONUNBUFFERED=1
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir --upgrade pip && \
    pip install --no-cache-dir -r requirements.txt
COPY app.py .
RUN useradd --system --uid 10001 --no-create-home appuser
USER appuser
EXPOSE 5000
ARG APP_VERSION=dev
ENV APP_VERSION=${APP_VERSION}
CMD ["python", "app.py"]
