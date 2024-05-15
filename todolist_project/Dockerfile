# python 3.8 이미지로 새로운 이미지 생성 -> 컨테이너 생성
FROM python:3.8

# 컨테이너 내의 작업 디렉토리를 /app 으로 설정
WORKDIR /app

# 현재 호스트 머신의 디렉토리와 파일을 컨테이너의 /app에 복사
COPY . /app

# requirements.txt 에 명시된 python 패키지 설치
# --no-cache-dir 으로 pip이 패키지를 캐시하지 않도록 하여 이미지 크기를 줄임
RUN pip install --no-cache-dir -r requirements.txt

# 컨테이너가 시작될 때 실행할 명령 설정
# Django 개발 서버를 0.0.0.0:8000 에서 실행
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
