# DB-link

//자바 DB연결

//여기에 DB테이블 생성 쓰기

# jsp파일에 db연결하기
# 1. join.jsp
![1](https://user-images.githubusercontent.com/104752580/186064466-c9182bee-4cd6-433b-aa94-679dda1e8e53.JPG)
### member_tbl_02 테이블에서 custno에 max값을 이용해서 마지막에 있는 값을 출력받고 1을 더해서 자동완성 시켜주는 코드입니다.
![2](https://user-images.githubusercontent.com/104752580/186064469-173f332c-ace2-45d9-ac00-cbee67a90241.JPG)
### 실행 되었을때 빈칸이 다 채워져 있는지 확인할 수 있도록 checkValue 함수를 써서 유효성 검사를 하고 빈칸이 있다면 그것에 맞게 다시 입력하라는 문구를 띄워준후에 빈칸으로 커서가 바뀌는 코드입니다. 
![3](https://user-images.githubusercontent.com/104752580/186064480-77a584f9-0455-4c11-8126-c263f3bec583.JPG)
### form 태그를 이용하여 join_p.jsp 파일과 연결 시켜주었습니다. 그리고 테이블을 이용하여 입력하는 곳을 만들고 버튼 세개를 만들어서 등록을 누르면 멤버 테이블에 있는 회원 정보에 값에 추가가 되고 취소를 하면 다시 join.jsp로 오게 되고 조회를 하면 member_list.jsp로 가게하는 코드입니다.
# 2. join_p.jsp
![4](https://user-images.githubusercontent.com/104752580/186064527-1eda37ed-ba01-4f00-b8f7-37918d6a4493.JPG)
### join_p.jsp와 bd를 연동시켜서 7개에 값을 꽂아넣으면 멤버 테이블에 추가가 될수있게 만든 코드입니다.
회원번호는 자동발생하게 설정되어 있어서 6개를 string형으로 꽂아주게되면 pstmt.executeUpdate를 통해서 테이블에 추가가 됩니다.
추가가 끝나면 자동으로 인덱스 창으로 넘어갑니다.
# 실행화면&테이블
![5](https://user-images.githubusercontent.com/104752580/186064569-b672221a-4cf9-4986-8d17-edb8c56d80d3.JPG)
![6](https://user-images.githubusercontent.com/104752580/186064571-0962cd32-fdbb-4235-8b70-c1c87390a7d7.JPG)
![7](https://user-images.githubusercontent.com/104752580/186064575-62c98ffa-41f5-4c22-af31-c33451a278ad.JPG)
