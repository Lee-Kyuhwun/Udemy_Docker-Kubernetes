# node:14 이미지를 기반으로 새 Docker 이미지를 생성합니다.
FROM node:14

# /app 이라는 디렉토리를 컨테이너 내에 작업 디렉토리로 설정합니다.
WORKDIR /app

# package.json 파일을 현재의 작업 디렉토리(/app)에 복사합니다.
COPY package.json .

# package.json에 명시된 npm 패키지들을 설치합니다.
RUN npm install

# 현재 디렉토리의 모든 파일과 폴더(.의 의미)를 컨테이너의 /app 디렉토리에 복사합니다.
COPY . .

# 컨테이너의 3000번 포트를 외부에 노출시킵니다.
EXPOSE 3000

# 컨테이너가 실행될 때 "node app.mjs" 명령을 실행하도록 설정합니다. 
CMD [ "node", "app.mjs" ]
