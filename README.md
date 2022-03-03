# 프로젝트 설명
등대99

항해99를 진행하면서 나누고 싶은 지식이나 정보를 공유하는 사이트입니다.

부트캠프라는 망망대해를 항해하는 과정에서 수강생들의 등대 역할을 하는 사이트를 만들고자 이런 이름을 선택하였습니다.

항해99의 공지사항부터 항해 과정에 도움이 될 자료들을 비롯해 알아두면 좋을 블로그나 유튜브 링크들까지.

99일 동안 항해하며 크루원들이 길을 잃지 않고 멋지게 성장할 수 있도록 길을 비추겠습니다.


# 기능 

기능 나열 

| 기능 | Method | URL | request | response |
| -- | -- | -- | -- | -- |
|포스팅 목록 전체 불러오기|GET| /api/reviews||전체 포스팅|
|카테고리 별로 포스팅 목록 가져오기 |GET|/api/category|Posting {"Category ": Category}|카테고리 포스팅 리스트|
글 포스팅 하기 | POST |/api/post_write
글 삭제 하기 | DELETE |/api/post_delete
상세 페이지 열기|GET |/api/post_view
좋아요|POST|/api/like|Posting{’id’:id}|좋아요 + 1|
로그인|POST|/api/sign_in|User {"ID" : ID,"Password" : password}
회원 가입|POST|/api/sign_up|User {"ID" : ID,"Password" : password,"Nicname" : name,"writepost" : [],"Readpost" : []}|
회원 탈퇴|DELETE|/api/sign_delete|User {"ID" : ID}



와이어프레임 대로 뷰 만들기

메인페이지 프레임 구현
로그인/회원가입 페이지 모달로 구현
햄버거 메뉴
상세페이지 구현

# DB Schema

User {
    "ID" :  ID,
	"Password" : password,
    "Nicname" : name,
    "writepost" : { "Category" : Category, "Title" : title },
    "Readpost" : { "Category" : Category, "Title" : title }
}


posting {
    "ID" : ID,
	"Category ": Category,
    "Title" : title,
	"Author" : author,
	"Date" : date,
	"Content" : content,
	"like" : 0
}

# 와이어 프레임

![와이어 프레임](https://images.velog.io/images/shine7329/post/557dcb77-9fad-4fd6-89c9-d72e2b0807d9/image.png)

