# swarmFabric

4 Peer 2 Org

**CLI 생성 파일에서 Volumes:에 모든 volume이 추가 되어있지 않을수도 있으니 추가 확인하시오**


사용방법: 

1. 스웜 세팅
     docker swarm init --advertise-addr <host-1 ip address>
     docker swarm join-token manager
     
     On Host 2
     <output from join-token manager> --advertise-addr <host n ip>
      
     On host 1,
     docker network create --attachable --driver overlay first-network

2. Container up 
     ./upNetwork.sh

3. 오류시 
     channel-artifacts 삭제
     crypto-config 삭제 
     ./basic.sh
