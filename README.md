# 설명
william.wow.wrtn.ai/chat-room/<room_id> 부분에 PUT 메소드로 내용은 {} 으로 보내면 채팅방의 설정과 정보에 대해서 응답해주고
PUT 메소드로 캐릭터챗 정보를 양식대로 보내면 해당 치팅방id의 캐릭터 챗 정보를 권한제한없이 임의로 수정 가능함이 확인되었습니다.

아래 로그는 세이프티봇을 임의로 수정해 "character"의 "isAdult" 항목을 수정한것입니다.
*참고* 
isAdult를 false 에서 true로 설정할려하면 isAudult 항목이 사라지는걸 확인했습니다. 이후 해당 채팅방에서 확인결과 세이프티봇이 언세이프티봇이 된것을 확인했습니다.(OOC 제제나 특정단어 검열이 아예 사라짐)
언세이프티 항목은 세이프티화 시킬수없음이 확인됬습니다.
# 요청
```
PUT /chat-room/67736db19657f4246b91c52b HTTP/2
Host: william.wow.wrtn.ai
Content-Length: 2
Sec-Ch-Ua-Platform: "Windows"
Authorization: Bearer <token>
Sec-Ch-Ua: "Google Chrome";v="131", "Chromium";v="131", "Not_A Brand";v="24"
Wrtn-Locale: ko-KR
Sec-Ch-Ua-Mobile: ?0
Mixpanel-Distinct-Id: 6758744780dc101d13688517
X-Wrtn-Id: <id>
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36
Accept: application/json, text/plain, */*
Content-Type: application/json
Platform: web
Origin: https://wrtn.ai
Sec-Fetch-Site: same-site
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: https://wrtn.ai/
Accept-Encoding: gzip, deflate, br
Accept-Language: ko-KR,ko;q=0.9,en-US;q=0.8,en;q=0.7
Priority: u=1, i

{}
```

# 응답
```
HTTP/2 200 OK
Date: Tue, 31 Dec 2024 04:06:40 GMT
Content-Type: application/json; charset=utf-8
Content-Security-Policy: default-src 'self';base-uri 'self';font-src 'self' https: data:;form-action 'self';frame-ancestors 'self';img-src 'self' data:;object-src 'none';script-src 'self';script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests
Cross-Origin-Embedder-Policy: require-corp
Cross-Origin-Opener-Policy: same-origin
Cross-Origin-Resource-Policy: same-origin
X-Dns-Prefetch-Control: off
X-Frame-Options: SAMEORIGIN
Strict-Transport-Security: max-age=15552000; includeSubDomains
X-Download-Options: noopen
X-Content-Type-Options: nosniff
Origin-Agent-Cluster: ?1
X-Permitted-Cross-Domain-Policies: none
Referrer-Policy: no-referrer
X-Xss-Protection: 0
Access-Control-Allow-Origin: *
Etag: W/"3d2-cZS4P2TQEI2MWChB7XrpRN2azys"
Vary: Accept-Encoding
Cf-Cache-Status: DYNAMIC
Server: cloudflare
Cf-Ray: 8fa765f32910d555-NRT

{
  "result": "SUCCESS",
  "data": {
    "_id": "67736db19657f4246b91c52b",
    "userId": "6758744780dc101d13688517",
    "model": "SONNET",
    "isDeleted": false,
    "version": "1.2.0",
    "shareChatIds": [],
    "character": {
      "_id": "6738b48ec4bc1d1deb5bf739",
      "snapshotId": "674af489fbaa185fcbc3159a",
      "name": "아카데미의 환생자",
      "profileImage": {
        "origin": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5.webp",
        "w200": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5_w200.webp",
        "w600": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5_w600.webp"
      },
      "startingSetId": "6742c1c369b24c360e7b8eda",
      "isAdult": false,
      "userNoteId": "67736db19657f4246b91c534"
    },
    "messagedAt": "2024-12-31T04:06:11.140Z",
    "createdAt": "2024-12-31T04:06:09.925Z",
    "updatedAt": "2024-12-31T04:06:11.407Z",
    "__v": 0,
    "topic": "gg"
  }
}
```

# 요청
```
PUT /chat-room/67736db19657f4246b91c52b HTTP/2
Host: william.wow.wrtn.ai
Content-Length: 671
Sec-Ch-Ua-Platform: "Windows"
Authorization: Bearer <token>
Sec-Ch-Ua: "Google Chrome";v="131", "Chromium";v="131", "Not_A Brand";v="24"
Wrtn-Locale: ko-KR
Sec-Ch-Ua-Mobile: ?0
Mixpanel-Distinct-Id: 6758744780dc101d13688517
X-Wrtn-Id: <id>
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/131.0.0.0 Safari/537.36
Accept: application/json, text/plain, */*
Content-Type: application/json
Platform: web
Origin: https://wrtn.ai
Sec-Fetch-Site: same-site
Sec-Fetch-Mode: cors
Sec-Fetch-Dest: empty
Referer: https://wrtn.ai/
Accept-Encoding: gzip, deflate, br
Accept-Language: ko-KR,ko;q=0.9,en-US;q=0.8,en;q=0.7
Priority: u=1, i

{
  "character": {
    "_id": "6738b48ec4bc1d1deb5bf739",
    "snapshotId": "674af489fbaa185fcbc3159a",
    "name": "아카데미의 환생자",
    "profileImage": {
      "origin": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5.webp",
      "w200": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5_w200.webp",
      "w600": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5_w600.webp"
    },
    "startingSetId": "6742c1c369b24c360e7b8eda",
    "isAdult": false,
    "userNoteId": "67736db19657f4246b91c534"
  }
}
```
# 응답
```
HTTP/2 200 OK
Date: Tue, 31 Dec 2024 04:09:34 GMT
Content-Type: application/json; charset=utf-8
Content-Security-Policy: default-src 'self';base-uri 'self';font-src 'self' https: data:;form-action 'self';frame-ancestors 'self';img-src 'self' data:;object-src 'none';script-src 'self';script-src-attr 'none';style-src 'self' https: 'unsafe-inline';upgrade-insecure-requests
Cross-Origin-Embedder-Policy: require-corp
Cross-Origin-Opener-Policy: same-origin
Cross-Origin-Resource-Policy: same-origin
X-Dns-Prefetch-Control: off
X-Frame-Options: SAMEORIGIN
Strict-Transport-Security: max-age=15552000; includeSubDomains
X-Download-Options: noopen
X-Content-Type-Options: nosniff
Origin-Agent-Cluster: ?1
X-Permitted-Cross-Domain-Policies: none
Referrer-Policy: no-referrer
X-Xss-Protection: 0
Access-Control-Allow-Origin: *
Etag: W/"3c2-ESwGG7gWOjcEGhn8GIQfWfY6FK0"
Vary: Accept-Encoding
Cf-Cache-Status: DYNAMIC
Server: cloudflare
Cf-Ray: 8fa76a360c4d685d-NRT

{
  "result": "SUCCESS",
  "data": {
    "_id": "67736db19657f4246b91c52b",
    "userId": "6758744780dc101d13688517",
    "model": "SONNET",
    "isDeleted": false,
    "version": "1.2.0",
    "shareChatIds": [],
    "character": {
      "_id": "6738b48ec4bc1d1deb5bf739",
      "snapshotId": "674af489fbaa185fcbc3159a",
      "startingSetId": "6742c1c369b24c360e7b8eda",
      "name": "아카데미의 환생자",
      "profileImage": {
        "origin": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5.webp",
        "w200": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5_w200.webp",
        "w600": "https://wrtn-image-ai-character.s3.ap-northeast-2.amazonaws.com/8D6bovHnvZC-NVKOOUtYRlJT/4a42dd8e-bd80-45e0-9f5e-f032e3b5c4b5_w600.webp"
      },
      "userNoteId": "67736db19657f4246b91c534"
    },
    "messagedAt": "2024-12-31T04:06:11.140Z",
    "createdAt": "2024-12-31T04:06:09.925Z",
    "updatedAt": "2024-12-31T04:09:34.455Z",
    "__v": 0,
    "topic": "gg"
  }
}
```
