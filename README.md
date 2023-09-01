# FULLSTACK SETTINGS / NEXT+EXPRESS

Author: Jaekyeong Yuk

풀스택 프로젝트 개발 시 사용하는 툴과 파일 구조 및 규칙들을 정립하여 패키지로 관리한다.

### FRONTEND

> 파일 구조 및 네이밍 규칙

- 페이지 구분: 디렉토리
- 하나의 디렉토리는 서버 컴포넌트(page.tsx), 클라이언트 컴포넌트(page.client.tsx), 서버 레이아웃 컴포넌트(layout.tsx, 선택사항), 클라리언트 레이아웃 컴포넌트(layout.client.tsx, 선택사항)가 존재. (비동기 요청 없는 경우 클라이언트 컴포넌트만 존재)
- 비동기 요청: GET은 hooks/queries, Mutation이 필요한 나머지 요청들은 hooks/mutations에서 관리.
- 부분 컴포넌트: 모든 레이아웃에서 쓰이는 공통 컴포넌트는 components/common, 나머지는 디렉토리로 구분하여 관리.

> Packages

- Base: TypeScript React React-query Framer-motion
- Server: Next
- Style: Emotion Tailwind
- Convention: ESlint Prettier

> Settings

```bash
npm i
npm run dev
```

### BACKEND

> Packages

- Server: Express
- Authentication: Passport
- Database: MySQL

> Settings

```bash
npm i
npx sequelize db:create
npm run dev
```

```bash
* dotenv 파일 설정
COOKIE_SECRET=secret
DB_PASSWORD=mysql-password
KAKAO_CLIENT_ID=id
GOOGLE_ID=id
GOOGLE_SECRET=secret
MAIL_ADDRESS=email
MAIL_APP_PASSWORD=password

```

> Reference

- Server/Client Components Used

  ![image](https://github.com/yjglab/yjglab/assets/70316567/0d2bf957-1ae5-4d6e-826d-d10230fe432b)
