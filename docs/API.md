# API 명세

---

## POST /api/auth/signup - 회원가입

- Description
    - 회원 가입
- Request

```
  {
    "username": "Strnig - 유저 이름(아이디)",
    "password": "String - 비밀번호"
  }
```

- Response

```
  {
    "msg": "회원가입 성공",
    "statusCode": 200
  }
```

## POST /api/auth/login - 로그인

- Description
    - 로그인
- Request

```
  {
    "username": "Strnig - 유저 이름(아이디)",
    "password": "String - 비밀번호"
  }
```

- Response

```
  {
    "msg": "로그인 성공",
    "statusCode": 200
  }
```

## POST /api/posts - 게시글 작성

- Description
    - 게시글 작성
- Request

```
  {
    "title": "String - 제목",
    "username": "String - 작성자명",
    "password": "String - 비밀번호",
    "content": "String - 내용"
  }
```

- Response

```
  {
    "id": "Long - 게시글 아이디",
    "title": "String - 제목",
    "content": "String - 내용",
    "username": "String - 작성자명",
    "createdAt": "LocalDateTime - 생성일시"
  }
```

## GET /api/posts - 게시글 목록 조회

- Description
    - 게시글 목록 조회
- Response

```
  [
    {
      "id": "Long - 게시글 아이디",
      "title": "String - 제목",
      "content": "String - 내용",
      "username": "String - 작성자명",
      "createdAt": "LocalDateTime - 생성일시"
    }
  ]
```

## GET /api/posts/{id} - 게시글 상세 조회

- Description
    - 게시글 상세 조회
- Response

```
  {
    "id": "Long - 게시글 아이디",
    "title": "String - 제목",
    "content": "String - 내용",
    "username": "String - 작성자명",
    "createdAt": "LocalDateTime - 생성일시"
  }
```

## PUT /api/posts/{id} - 게시글 수정

- Description
    - 게시글 수정
- Request

```
  {
    "title": "String - 제목",
    "content": "String - 내용"
    "password": "String - 비밀번호"
  }
```

- Response

```
  {
    "id": "Long - 게시글 아이디",
    "title": "String - 제목",
    "content": "String - 내용",
    "username": "String - 작성자명",
    "createdAt": "LocalDateTime - 생성일시"
  }
```

## DELETE /api/posts/{id} - 게시글 삭제

- Description
    - 게시글 삭제
- Request

```
  {
    "password": "String - 비밀번호"
  }
```

- Response

```
  {
    "msg": "게시글 삭제 성공",
    "statusCode": 200
  }
```