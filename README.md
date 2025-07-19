# War of Gods
# WoG

플러그인과의 충돌을 막기 위해 최소한의 명령어로 작동하도록 제작하였습니다.
의뢰인의 의뢰 변경으로 인해 두 팀 버전으로 데이터팩을 재구성하였습니다.

각각의 팀의 리스폰을 담당하는 침대를 제공하며, 킬 수에 비례한 부활 시간 조정하는 기능을 제공합니다.

1. 아이템 액자 속 해당 팀 침대를 끼워 팀 침대를 설치할 수 있습니다.
2. 소속된 팀이 없을 경우 소속 인원이 적은 팀으로 자동 소속됩니다.
3. 서바이벌 모드가 아닌 경우 침대를 부술 수 없습니다.
4. 서바이벌 모드인 경우 적팀의 침대만 부술 수 있습니다.
5. 서바이벌 모드인 경우 시스템을 통해 부활 시간이 조정됩니다.
6. 침대를 완전히 제거하기 위해서는 적팀의 상태에 서바이벌 모드로 침대를 파괴한 후 크리에이티브 모드에서 액자를 부술 수 있습니다.

지원하는 명령어를 확인할 수 있습니다.  
`/function war:config`

팀, 침대, 탈락 여부 등 데이터팩 관련 진행요소들을 준비 상태로 설정합니다.  
`/function war:config/reset`

팀에 참가합니다.  
`/team join <color> <targets>`  

해당 플레이어 상태를 첫 접속한 서버 상태로 변경합니다.  
`/advancement revoke <targets> only war:tags/init`

아래 공식을 기준으로 부활 시간을 조정합니다.  
* 킬 수(playerKill) * 단위 초(multiRespawn) + 기본 초(addSec)  
`/scoreboard players set multiRespawn config 2`  
`/scoreboard players set addRespawn config 0`  
