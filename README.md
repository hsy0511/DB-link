# DB-link
# jsp파일에 db연결하기
# 실행화면&테이블
![5](https://user-images.githubusercontent.com/104752580/186064569-b672221a-4cf9-4986-8d17-edb8c56d80d3.JPG)
![6](https://user-images.githubusercontent.com/104752580/186064571-0962cd32-fdbb-4235-8b70-c1c87390a7d7.JPG)
![7](https://user-images.githubusercontent.com/104752580/186064575-62c98ffa-41f5-4c22-af31-c33451a278ad.JPG)
# DB테이블 생성
![8](https://user-images.githubusercontent.com/104752580/186090547-191f0123-e910-4374-8a08-9f296e6aed76.JPG)
# 자바 DB연결
![9](https://user-images.githubusercontent.com/104752580/186090575-5a74baeb-eddf-444a-aacf-a9041deba32e.JPG)
### db가 system계정에 연결이 성공했을시 db test라는 문구가 출력됩니다.
# 1. join.jsp
![1](https://user-images.githubusercontent.com/104752580/186064466-c9182bee-4cd6-433b-aa94-679dda1e8e53.JPG)
### 회원번호를 자동발행을 시키기 위해서 member_tbl_02 테이블에있는 custno에 max값을 이용해서 마지막에 있는 값을 출력받고 num 값에는 마지막에 있는 값에 1을 더해주는 코드입니다.
![2](https://user-images.githubusercontent.com/104752580/186064469-173f332c-ace2-45d9-ac00-cbee67a90241.JPG)
### 실행 되었을때 빈칸이 다 채워져 있는지 확인할 수 있도록 checkValue 함수를 써서 유효성 검사를 하고 빈칸이 있다면 그것에 맞게 다시 입력하라는 문구를 띄워준후에 빈칸으로 커서가 바뀌는 코드입니다. 
![3](https://user-images.githubusercontent.com/104752580/186064480-77a584f9-0455-4c11-8126-c263f3bec583.JPG)
### form 태그를 이용하여 join_p.jsp 파일과 연결 시켜주었습니다. 그리고 테이블을 이용하여 입력하는 곳을 만들고 회원번호는 아까 마지막 값에 1을 더한 값을 자동발생 시키게 했습니다. 그리고 버튼 세개를 만들어서 등록을 누르면 멤버 테이블에 있는 회원 정보에 값에 추가가 되고 취소를 하면 다시 join.jsp로 오게 되고 조회를 하면 member_list.jsp로 가게하는 코드입니다.
# 2. join_p.jsp
![4](https://user-images.githubusercontent.com/104752580/186064527-1eda37ed-ba01-4f00-b8f7-37918d6a4493.JPG)
### join_p.jsp와 bd를 연동시켜서 7개에 값을 꽂아넣으면 멤버 테이블에 추가가 될수있게 만든 코드입니다.
### 회원번호는 형변환를 시켜서 integer형으로 받아주고 다른 6개는 get.parameter를 통해 사용자가 적은 값을 string형으로 세팅해주고 pstmt.executeUpdate를 통해서 테이블에 추가가 됩니다.
### (회원번호는 자동발생하게 설정되어 있어서 안적어도 됨.)
### 추가가 끝나면 자동으로 인덱스 창으로 넘어갑니다.
