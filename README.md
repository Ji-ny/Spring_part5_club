# Spring_part5_club


---

### 1. 이메일 데이터 생성

![image](https://user-images.githubusercontent.com/96537605/185401645-6472a6f9-fa74-407d-82f5-af1f584d1375.png)
![image](https://user-images.githubusercontent.com/96537605/185401702-fb65df3d-babc-432e-91ba-993eca511173.png)
- **club_member 테이블**
    - 회원 정보 기록
- **club_member_role_set 테이블**
    - 권한 기록

### 2. 로그인 실패
![image](https://user-images.githubusercontent.com/96537605/185401734-7f391763-85ea-43ec-a7af-6fd1725242b6.png)
- 올바른 아이디와 비밀번호를 입력하지 않으면 에러 문구가 발생한다.

---

### 1. 구글 프로젝트에 현재 프로젝트 등록

[API 및 서비스 – Google Cloud Console](https://console.cloud.google.com/)

1. **Oauth클라이언트** 

![image](https://user-images.githubusercontent.com/96537605/185401777-dd9e9b1b-d6e6-4e52-9978-7ea962d8973c.png)
- 클라이언트 생성 뒤 아이디와 비밀번호를 받는다.

**1-1. 결과 : 생성된 OAuth 클라이언트**

![image](https://user-images.githubusercontent.com/96537605/185401836-6ed87806-9fb9-4946-b4ca-338c8f8c2da9.png)- 생성완료

### 2. 로그인 화면

- [Please sign in](http://localhost:8080/login)

![image](https://user-images.githubusercontent.com/96537605/185401856-3baf1c89-c538-4175-a9e8-06ac79b7ba21.png)
- 구글을 통한 로그인과, 일반 로그인이 가능하다.
- Remember me 체크 박스를 클릭하면, 7일간 아이디와 비밀번호 쿠키를 저장한다.

### 3. Member 확인

![image](https://user-images.githubusercontent.com/96537605/185401891-5bc12620-b7a7-4d85-9a55-7246f06b4d80.png)
- 현재 접속한 계정을 확인할 수 있다.

### 4. 사용자 추가

![image](https://user-images.githubusercontent.com/96537605/185401927-50dc5319-88c9-4f6d-887f-6629b5ec8569.png)
- user 사용자와 구글 사용자를 추가했다.

### 5. 접근 제한

- user95 계정으로만 /localhost:8080/sample/admin 접속 시, 접속이 가능하다.

---

### 1. 인증 실패 처리

![image](https://user-images.githubusercontent.com/96537605/185401953-39326de1-5850-4e38-9080-aff10df5564d.png)
- 인증이 불가능한 정보를 전송하면, 401상태 코드와 함께 에러가 전송된다.

### 2. 인증 성공 처리

- [http://localhost:8080/api/login?email=user90@zerock.org&pw=1111](http://localhost:8080/api/login?email=user90@zerock.org&pw=1111)
- 정상적인 계정 정보를 입력하면, 정상적인 동작 로그가 출력된다.

### JWT 처리

→ [localhost:8080/api/login?email=user90@zerock.org&pw=1111](http://localhost:8080/api/login?email=user90@zerock.org&pw=1111)

![image](https://user-images.githubusercontent.com/96537605/185402000-cc180f2b-f943-483b-be17-c7831324db68.png)
- JWT가 발행된 것을 알 수 있다.
