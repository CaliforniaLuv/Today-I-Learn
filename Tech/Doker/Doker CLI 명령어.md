

# CLI 명령어

<br/>

## Container 생성


```
  docker run Image명 
```

Doker hub에 ```pull```하여 받아온 Image를 ```run```하여 Container를 생성한다. ( *생성 동시에 Container는 실행 상태* )

<br/>
<br/>

## Container 이름 직접 생성


```
  docker run --name 홍길동 Image명
```

생성된 Container의 이름은 홍길동이 된다.

<br/>
<br/>


## Container port 설정 후 생성


```
  docker run --name 홍길동 -p 80:8080 Image명
```

80은 Doker의 ```Host```의 포트이고, 8080은 ```Container```의 포트이다.

```
CONTAINER ID   IMAGE          COMMAND              CREATED          STATUS          PORTS                          NAMES
d1a2109a5858   httpd          "httpd-foreground"   18 seconds ago   Up 2 seconds    80/tcp, 0.0.0.0:80->8080/tcp   홍길동
```

Port를 해석하자면 0.0.0.0:80 이라는 Host port가 홍길동 Container에 접속하기를 희망한다면, 8080 port와 연결해야 한다.


<br/>
<br/>

## 생성된 Container 조회


```
  docker ps
```

<br/>
<br/>

## 모든 Container 조회 ( *정지된 Container도 조회* )


```
 docker ps -a
```

생성된 Container를 조회한다.

<br/>
<br/>

## 실행된 Container 정지


```
  docker stop ws2
```

<br/>
<br/>

## Container 실행

```
  docker start 홍길동
```

홍길동이라는 Container가 다시 실행된다.

<br/>
<br/>

## Container Log 조회


```
  docker logs 홍길동
```

홍길동이라는 Container의 Log를 조회할 수 있다.(실시간 X)

```  
  docker -logs -f 홍길동
```

홍길동이라는 Container의 Log를 실시간 조회할 수 있다.

<br/>
<br/>


## Container 삭제

```
  docker rm 홍길동
```

Container 실행 정지 후 삭제가 가능하다.

<br/>
<br/>

## 실행 중인 Container 즉시 삭제

```
  docker rm --force 홍길동
```

Container 실행 정지 후 삭제가 가능하다.

<br/>
<br/>

## Image 삭제


```
  docker rmi httpd
```

해당 Image의 모든 Container가 삭제되어야(빈 상태) Image를 삭제할 수 있다.

<br/>
<br/>
