
## CentOS7 iso 다운로드

URL : http://mirror.anigil.com/CentOS/7.9.2009/isos/x86_64/

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/47aab3ad-dd69-44c2-bbc2-ecaf7c8883e9)

## VMware 세팅

Create a New  Virtual Machine<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/97df804c-c0d1-4ec0-8e6c-b5b86fde345b)

이미지 설정<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/98cf80bb-4c65-4b4c-a113-90099ff3241f)

경로<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/110c6821-6e04-4544-a550-7631814e52f8)

드라이버 용량<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/6a57c3ca-287b-4898-aba3-63f02a41355d)

메모리 4gb
프로세스 4<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/f86af3d0-724b-410a-9dd8-afdd7ebd101d)

## CentOS7 Setting

언어 설정<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/0f18e5fd-82c3-42a8-ad6f-e054290365d5)


디스크 설정<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/bcaea6d8-10d2-440e-b620-db2e61e9ef57)

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/996f1c54-c644-4d9a-9289-b097720b5d76)

설치 시작<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/b079f740-2a94-4aec-96d1-a0fdf3694dca)

ROOT 암호 설정<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/33c6e5ef-9cc6-40a4-8363-fc9bc313110f)

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/f7977737-ef10-491e-8836-0ceb258755e9)

ROOT 로그인<br/>
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/d51e82d0-fd5c-481e-b12e-1c1eee1a18e6)

## MobaXterm Connect

설치 : https://mobaxterm.mobatek.net/download-home-edition.html

### IP 세팅 및 확인

vi를 이용하여 /etc/sysconfig/network-scripts/ifcfg-ens33 설정

BOOTPROTO의 값을 static로 변경

IPADDR= 사용할 IP주소 <br/>
NETMASK =서브넷 마스크 <br/>
GATEWAY= 게이트웨어 주소 <br/>
ONBOOT= yes <br/>

속성 추가

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/b6741a48-b0b3-493c-9a26-0753395c5421)


재부팅 후 ip addr 커맨드로 ip 확인
![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/e264fa2a-83d0-474c-846a-3f9231cf1b11)

세션 세팅 & 접속

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/dbd64044-657b-4672-9aaf-fc1a14a488f3)

![image](https://github.com/LeeJaeYong02/Oacle-Tuning-Essentials/assets/66985977/5f093638-5693-4a5e-b231-78ed05b4a149)


