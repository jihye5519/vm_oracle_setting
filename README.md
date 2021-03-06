## <VM ware 등록 후 (D드라이브 생성)>


### 1. VM images 등록
<img src="./img/1.vm images 등록.png" width="800px" height="400px">


### 2. 생성된 vm 디스크 용량 확장
<img src="./img/2.생성된 vm 디스크 용량 확장.png" width="700px" height="400px">


### 2-1 SCSI 확장 크기 입력 후 생성
<img src="./img/3.용량입력.png" width="700px" height="400px">


### 3. 내컴퓨터 > 관리> 디스크 관리 > 생성한 드라이브 문자 및 경로 변경
<img src="./img/4.파티션 생성.png" width="700px" height="400px">


## <오라클 설치>

### 4. 오라클 설치
<img src="./img/오라클설치1.png" width="700px" height="400px">

<img src="./img/오라클설치2.png" width="700px" height="400px">

<img src="./img/오라클설치3.png" width="700px" height="400px">

<img src="./img/오라클설치4.png" width="700px" height="400px">

<img src="./img/오라클설치5.png" width="700px" height="400px">

<img src="./img/오라클설치6.png" width="700px" height="400px">

<img src="./img/오라클설치8.png" width="700px" height="400px">

<img src="./img/오라클설치9.png" width="700px" height="400px">

## <오라클 셋팅>

#### 5. SQL Plus 실행
오라클을 설치하면 SQL Plus가 만들어지는데 접속이 잘 되는지 먼저 확인한다.
<img src="./img/DB셋팅1.png" width="700px" height="400px">

#### 5-1 sqldeveloper 실행 후 셋팅
<img src="./img/DB셋팅7.png" width="700px" height="400px">
<img src="./img/DB셋팅8.png" width="700px" height="400px">
 
#### 5-2 DB정보 입력

오라클 설치할 때 설정한 정보를 입력하고 하단에 테스트 버튼을 눌러서 접속이 잘 되었는지 확인한다. 접속 실패 시 5-4 와 5-5 사항을 확인한다.
(호스트 이름은 localhost 또는 5-3에서 확인한 ip를 적어준다.)

<img src="./img/DB셋팅9.png" width="700px" height="400px">

#### 5-3 cmd창에서 아이피와 호스트이름 확인
<img src="./img/DB셋팅2.png" width="700px" height="400px">
<img src="./img/DB셋팅3.png" >

#### 5-4 오라클 설정파일 수정

D:\product\11.2.0\dbhome_1\NETWORK\ADMIN 경로에 listener.ora 와 tnsnames.ora 파일을 열어서 localhost 부분을 5-3에서 확인 호스트 이름으로 변경해준다.

<img src="./img/DB셋팅4.png" width="700px" height="400px">
<img src="./img/DB셋팅5.png" width="700px" height="400px">

#### 5-5 서비스 > 오라클 관련 서비스 시작 후 재접속 해보면 연결이 된다.
<img src="./img/DB셋팅10.png" width="700px" height="400px">


## <오라클 계정 생성>

#### 6. sqlplus 관리자 계정인 system 으로 접속 한 후 test 계정을 생성한다.
<img src="./img/DB셋팅12.png" width="700px" height="400px">

#### 6-1 생성한 계정에 모든 권한을 부여한다.
<img src="./img/DB셋팅13.png" width="700px" height="400px">

#### 6-2 생성한 계정으로 sqldeveloper 접속
<img src="./img/DB셋팅14.png" width="700px" height="400px">

#### 6-3 대용량 쿼리문은 DB툴에서 실행이 안되는 문제가 발생. 따라서 SQL plus에서 쿼리문을 실행해준다.
#### Window 환경 오라클 Sql plus에서 .sql 파일 직접 실행하기(대용량 sql문)

<img src="./img/DB셋팅15.png" width="700px" height="400px">

#### 6-4 데이터가 잘 삽입된 것을 확인할 수 있다.
<img src="./img/DB셋팅16.png" width="700px" height="400px">


## <외부PC → VM에 설치한 oracle DB IP에 접근> 

### 7. 고급 보안이 포함된 방화벽 처리
<img src="./img/5.방화벽처리.png" width="700px" height="400px">

#### 7-1 인바운드 규칙 등록
<img src="./img/6.인바운드 규칙생성_1.png" width="700px" height="400px">

#### 7-2 인바운드 규칙 등록
<img src="./img/6.인바운드 규칙생성_2.png" width="700px" height="400px">

#### 7-3 인바운드 규칙 등록
<img src="./img/6.인바운드 규칙생성_3.png" width="700px" height="400px">

### 7-4 VM setting > network adapter > Bridged로 선택 되어 있는지 체크
<img src="./img/7.vm setting.png" width="700px" height="400px">

### 7-5 외부 PC DB툴(Dbeaver)에서 정보 입력 후 연결하면 성공적으로 연결된다.
<img src="./img/DB셋팅11.png" width="700px" height="400px">



