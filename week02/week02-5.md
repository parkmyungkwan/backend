## Annotation
- @RequestMapping: HTTP Request로 들어오는 url을 특정 Controller 클래스나 메소드로 연결시느는 역할을 한다.   
보통 value와 method를 주로 사용하고 value는 요청받을 URL을 설정하고 method는 요청 메소드를 정의한다.
    - @GetMapping: HTTP Get Method에 해당하는 단축 표현(조회할때 사용)
    - @PostMapping: HTTP Post Method에 해당하는 단축 표현(등록할때 사용)
    - @PatchMapping: HTTP Patch Method에 해당하는 단축 표현(수정할때 사용)
    - @DeleteMapping: HTTP Delete Method에 해당하는 단축 표현(삭제할때 사용)
    - @PathVariable: URL 경로에 변수 값을 넣어서 사용