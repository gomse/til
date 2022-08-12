# Secure Copy

send files:
```bash
scp test1.file test2.file root@192.168.0.1:/tmp/test
```

send directory:
```bash
scp -r testdir root@192.168.0.1:/tmp/test
```

recv files:
```bash
scp root@192.168.0.1:/tmp/test.file ./

or

scp root@192.168.0.1:"/tmp/test1.file /tmp/test2.file" /tmp/
```

recv directory
```bash
scp -r root@192.168.0.1:/tmp/test /tmp/
```

options:
- `p`: 원본 권한 속성 유지
- `P`: 포트 번호 지정
- `c`: 압축
- `v`: 과정 출력
- `a`: 아카이브 모드

