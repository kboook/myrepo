유튜브 검색결과 화면의 소스를 이용해서
해당 결과의 영상들을
조회수 순으로 동영상 제목을 출력하는 프로그램

유튜브에 'python'을 검색한 결과화면의 url을 이용
"https://www.youtube.com/results?search_query=python"
여기서 영상 제목과 각 영상들의 조회수 정보를 가져와야 합니다.

페이지 소스의 패턴 상,
페이지 소스를 가져와서 string으로 변환 후
큰 따옴표(")로 split을 하면 영상의 제목, '게시자', '조회수', 조회수가 포함되는 원소들이 생깁니다.

    예: Python OOP Tutorial 1: Classes and Instances 게시자: Corey Schafer 2년 전 15분 조회수 839,931회

for 반복문과 if 조건문을 이용하여 '게시자'가 포함된 원소만 뽑아 리스트를 만들면
위 예와 같이 제목과 조회수의 정보가 있는 원소를 한 영상당 하나씩 가진 리스트가 생성됩니다.

for 반복문을 이용해 각 원소마다 '게시자'와 '조회수' 인덱싱을 활용하여
영상 제목과 조회수 정보를 딕셔너리에 저장합니다.

    영상 제목에 '게시자'나 '조회수'가 포함 될 수 있으므로 rfind()를 이용하고
    페이지 소스의 조회수 정보에는 839,931처럼 ','가 포함되므로 replace()를 이용해 처리해줍니다.
