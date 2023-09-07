# 노드js를 기본 이미지로 사용한다
FROM node:14
# 도커내 /app 폴더를 사용, 생성 (자체파일시스템, 작업하고자하는 특별한 디렉토리)
WORKDIR /app
# 작업 디렉토리에 종속성 및 패키지 버전을 복사 => npm install에 사용
COPY package.json .
# RUN으로 명령어 실행
RUN npm install
# 같은 경로에 다운로드 받은 파일을 복사해서 넣는다
COPY . .
# 어플리케이션 포트와 맞춤
EXPOSE 3000

CMD [ "node", "app.mjs" ]

# 명령어 
# docker build . => Dockerfile image 빌드
