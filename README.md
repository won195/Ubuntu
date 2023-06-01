# Ubuntu
Ubuntu
###마운트 포인트 설명
/ 루트 파티션
/bin 리눅스의 기본 명령어가 들어 있음
/sbin 시스템 관리용 명령어가 들어 있음
/etc 시스템 환경 설정과 관련된 파일이 들어 있음
/boot 부팅 커널을 저장
/media 외부 장치를 마운트 하기 위하여 사용
/usr 응용프로그램들을 주로 저장
/lib 프로그램들의 라이브러리가 저장됨
/deb 장치 파일들이 저장됨
/home 사용자별 공간
/root 시스템 관리자인 root 계정의 홈 디렉토리
/var 시스템 운영 중 발생한 로그, 캐시 파일들이 저장됨
/tmp 시스템 사용 중 발생한 임시 파일 저장(부팅 시 초기화)
#2. 리눅스 명령어 기초
모든 명령어는 --help 도움말 확인 가능 ex) shutdown --help
ubuntu@master:~$ sudo shutdown now
# shutdown 5
# shutdown -c
# shutdown -r now
*sudo
-superuser 권한으로 명령어 실행
*shutdown
시스템 종료, 명령어 다음에 종료 시간 설정 가능 (5분 뒤 종료)
--c : 시스템 종료 명령 취소
-now : 입력 즉시 명령어 실행
--r : 재시작
ubuntu@master:~$ sudo reboot
# sudo reboot -p
# sudo reboot -f
reboot
시스템 재시작
-p : poweroff, 시스템 종료
-f : force, 시스템 강제 재부팅
ubuntu@master:~$ pwd
/home/ubuntu
*pwd : Print Work Directory의 약자이며, 현재 사용자가 있는 디렉토리 출력
ubuntu@master:~$ ls -a
. Documents .local Spark_Workspace
.. Downloads .mozilla .ssh
.bash_history .gnupg Music .sudo_as_admin_successful
.bash_logout hadoop-env.sh Pictures Templates
.bashrc hadoop.tar.gz .profile Videos
.cache .ipynb_checkpoints Public .viminfo
.config .ipython .python_history .wget-hsts
Desktop .jupyter spark.tar.gz
ubuntu@master:~$ ls -al
total 1072476
drwxr-xr-x 20 ubuntu ubuntu 4096 5월 24 12:08 .
drwxr-xr-x 3 root root 4096 5월 15 10:59 ..
-rw------- 1 ubuntu ubuntu 13917 5월 31 18:10 .bash_history
-rw-r--r-- 1 ubuntu ubuntu 220 5월 15 10:59 .bash_logout
-rw-r--r-- 1 ubuntu ubuntu 4069 5월 24 10:22 .bashrc
drwx------ 14 ubuntu ubuntu 4096 5월 18 15:37 .cache
drwx------ 11 ubuntu ubuntu 4096 5월 15 11:07 .config
ls
list segments의 약자이며, 파일과 디렉터리의 모든 정보를 제공하며 특정 디렉터리와 특정 파일의 내용도
제공합니다.
-a : 숨김파일을 포함하여 디렉토리에 존재하는 포든 파일 출력
-l : 파일을 리스트 형식으로 출력
ubuntu@master:~$ cd Downloads/
ubuntu@master:~/Downloads$
cd
해당 디렉터리로 이동
ubuntu@master:~/Downloads$ mkdir test
ubuntu@master:~/Downloads$ ls
hadoop-3.3.5.tar.gz spark-3.4.0-bin-hadoop3.tgz test
mkdir
새 디렉토리 생성
ubuntu@master:~/Downloads$ rmdir test
ubuntu@master:~/Downloads$ ls
hadoop-3.3.5.tar.gz spark-3.4.0-bin-hadoop3.tgz
rmdir
remove directory의 약자이며, 빈 디렉터리를 삭제할 때 사용하는 명령어
디렉토리가 비어있지 않은 경우 삭제 불가능
