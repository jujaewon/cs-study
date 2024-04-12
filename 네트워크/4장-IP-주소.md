### 3계층의 기능

3계층에서 하는 일

- 3계층은 다른 네트워크 대역, 즉 멀리 떨어진 곳에 존재하는 네트워크까지 어떻게 데이터를 전달할지 제어하는 일을 담당
- 발신에서 착신까지의 패킷의 경로를 제어

3계층에서 쓰는 주소

- WAN에서 통신할 때 사용하는 IP 주소

IPv4 주소 : 현재 pc에 할당된 IP 주소

서브넷 마스크 : IP 주소에 대한 네트워크의 대역을 규정하는 것

게이트웨이 주소 : 외부와 통신할 때 사용하는 네트워크의 출입구

3계층의 프로토콜

IP 주소를 이용해 MAC 주소를 알아오는 ARP 프로토콜

WAN에서 통신할 때 사용하는 IPv4 프로토콜

서로가 통신되는지 확인할 때 사용하는 ICMP 프로토콜

### 일반적인 IP 주소

Classful IP 주소

낭비가 심한 Classful IP 주소

<table>
  <tr>
    <th style="text-align:center">클래스</th>
    <th style="text-align:center">네트워크 구분</th>
    <th style="text-align:center">시작 주소</th>
    <th style="text-align:center">마지막 주소</th>
  </tr>
  <tr>
    <td style="text-align:center">A 클래스</td>
    <td style="text-align:center">0XXXXXXX, 첫번째 필드</td>
    <td style="text-align:center">0.0.0.0</td>
    <td style="text-align:center">127.255.255.255</td>
  </tr>
  <tr>
    <td style="text-align:center">B 클래스</td>
    <td style="text-align:center">10XXXXXX, 두번째 필드</td>
    <td style="text-align:center">128.0.0.0</td>
    <td style="text-align:center">191.255.255.255</td>
  </tr>
  <tr>
    <td style="text-align:center">C 클래스</td>
    <td style="text-align:center">110XXXXX, 세번째 필드</td>
    <td style="text-align:center">192.0.0.0</td>
    <td style="text-align:center">223.255.255.255</td>
  </tr>
  <tr>
    <td style="text-align:center">D 클래스 (멀티캐스트)</td>
    <td style="text-align:center">1110XXXX</td>
    <td style="text-align:center">224.0.0.0</td>
    <td style="text-align:center">239.255.255.255</td>
  </tr>
  <tr>
    <td style="text-align:center">E 클래스 (예약)</td>
    <td style="text-align:center">1111XXXX</td>
    <td style="text-align:center">240.0.0.0</td>
    <td style="text-align:center">255.255.255.255</td>
  </tr>
</table>


낭비되지 않도록 아껴쓰는 Classless IP 주소

<table>
  <tr>
    <th colspan="2" style="text-align:center">192.168.32.189/26</th>
  </tr>
  <tr>
    <td>IP 주소</td>
    <td>192.168.32.189</td>
  </tr>
  <tr>
    <td>서브넷 마스크</td>
    <td>255.255.255.192</td>
  </tr>
  <tr>
    <td>네트워크 ID</td>
    <td>192.168.32.128</td>
  </tr>
  <tr>
    <td>브로드캐스트 주소</td>
    <td>192.168.32.191</td>
  </tr>
  <tr>
    <td>사용 가능 IP 범위</td>
    <td>192.168.32.129 ~ 192.168.32.190</td>
  </tr>
</table>

사설 IP와 공인 IP

공인 IP 1개당 2^32개의 사설 IP

실제 인터넷 세상에서는 공인 IP로만 통신
외부 네트워크 대역에서는 사설 IP 대역이 보이지 않는다.

### 특수한 IP 주소

Wildcard : 0.0.0.0
나 자신을 나타내는 주소 : 127.0.0.1
어딘가로 가려면 일단 게이트웨이 주소