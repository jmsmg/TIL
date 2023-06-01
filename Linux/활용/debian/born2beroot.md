# Born2beroot


- 프로그램 작동확인
    - systemctl status [프로그램]

- app-armor
    - aa-enabled

- UFW 실행 체크
    - sudo ufw status verbose
    - sudo ufw enable

- ip 확인
    - ip addr

- 네트워크 설정
    - /etc/network/interfaces
    - ss -tunpl 확인

- SSH 체크
    - /etc/ssh/sshd_config

- 유저 그룹체크
    - id

- 패스워드 정책 확인
    - 기간 /etc/login.defs
    - 비밀번호 /etc/pam.d/common-password
    - sudo chage -M 30 -m 2 -W 7 [유저이름]
    - chage -l [유저이름]

- retry=N : 암호입력을 N회로 설정
- minlen=N : 암호의 최소 길이는 N
- difok=N : 기존 패스워드와 달라야하는 문자 수 N
- ucredit=-N : 대문자 N개 이상 (N이 양수/음수인지 따라 뜻이 다름, 서브젝트 기준에 맞추어 음수로)
- lcredit=-N : 소문자 N개 이상 (위와 동일)
- decredit=-N : 숫자 N개 이상 (위와 동일)
- reject_username : 사용자의 이름이 그대로 혹은 뒤집혀 패스워드에 있는지 검사
- enforce_for_root : root사용자가 패스워드를 바꾸려 할 때에도 위 조건 적용
- maxrepeat=N : 같은 문자가 N번 이상 연속해서 나오는지 검사

- 새로운 유저 생성, 유저 세팅
    - groupadd [그룹명]
    - id [유저이름]
    - usermod -aG [그룹명] [유저이름]
    - primary그룹 설정 : usermod -g user42 [유저이름]

- 호스트네임, 파티션 확인
    - hostnamectl
    - sudo hostnamectl set-hostname [변경할 이름]
    - lsblk

- sudo 확인
    - visudo
    - var/log/sudo
    - 설치 확인 : dpkg -l sudo

- UFW 포트 확인, 새로운 포트 개방
    - ufw allow 4242
    - ufw status verbose

- ssh 개방, 포트 포워딩
    - ssh 유저이름@호스트ip -p 4242
    - ufw status numbered
