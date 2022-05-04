## 라라벨 개발환경 세팅

<br/>

라라벨 설치 참고 - Composer : [라라벨코리아:: 라라벨 9.x - 설치하기 (laravel.kr)](https://laravel.kr/docs/9.x/installation)

유튜브 라라벨 프레임 워크 : [Laravel 라라벨 기본기 익히기 1강 - 설치 - YouTube](https://www.youtube.com/watch?v=651rNimMy7w&list=PL-RB9oHEN4_9XDnPOvIP780IEBBIIMPDG)

PHP 참고 : [PHP: The Right Way (modernpug.github.io)](https://modernpug.github.io/php-the-right-way/)

라라벨 공식문서(영어) : [Installation - Laravel - The PHP Framework For Web Artisans](https://laravel.com/docs/9.x)

<br/>

### 1. Composer를 통한 설치

- 로컬개발서버가 됨 (배포용은 아닌듯 배포시에는 서버에 Docker나 NginX 위에 올려서 해야 하지 않을까)

1. [PHP 설치](https://windows.php.net/download#php-8.1) (zip 파일로)  
   - JAVA_HOME 처럼 PHP 환경변수도 설정해야하나봄  
   - php.exe 위치를 환경변수 파일 경로로 설정

2. [Composer (getcomposer.org)](https://getcomposer.org/) 설치  
	- 또는! https://laravel.kr/docs/7.x/installation  
	```composer global require laravel/installer```  
	아닌가? composer설치후 composer에 라라벨 인스톨러를 추가하는 거?
   
3. 라라벨 프로젝트 생성  
	```composer create-project --ignore-platform-req=ext-fileinfo --prefer-dist laravel/laravel blog```
	- 기본 형태 : `composer create-project laravel/laravel [my-app]`
	- `npx create-react-app [my-app]`와 비슷

4. 라라벨 실행  
	```php artisan serve```

※ 주의사항
composer가 설치시 php 버전에 dependency을 가지게 되는 듯
php 버전을 고정하고 사용하는게 오류가 안생길것 같다.
nvs처럼 php도 막 바꿀 수 있는줄 알았는데 그건 또 아닌가?
composer자체의 문제이기 보단 `composer create-project`를 하면 node처럼 지금 실행중인 버전으로 composer.json이 생성되서 안되나? 

<br/>

### 2. Docker를 통한 설치
???? 갑자기 WSL, Docker, Docker compose, Sail 개념이 흘러들어오는데 지금은 잘 모르겠음

<br/>

### 3. [Starter Kits : Breeze, Jetstream](https://laravel.com/docs/9.x/starter-kits)

#### 1. Breeze

1. 설치 
`composer require laravel/breeze --dev`
	- 설치가 안될 수 있음 -> `composer config -g -- disable-tls true` (안전하지 않아서 서버에 비추천한다고함...)


#### 2. Jetstream

<br/>


왤케 진행할수록 찝찝하냐
