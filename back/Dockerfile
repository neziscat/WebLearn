FROM python:3.13-slim

# 작업 디렉토리 설정
WORKDIR /app

# requirements 복사
COPY requirements.txt .

# 라이브러리 설치
RUN pip install --no-cache-dir -r requirements.txt

# 애플리케이션 코드 복사
COPY . .

EXPOSE 5000

# 기본 실행 명령 (필요에 따라 수정)
CMD ["uvicorn", "main:app", "--reload", "--host", "0.0.0.0", "--port", "5000"]