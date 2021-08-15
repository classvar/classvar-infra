## ClassVAR Infra Tech-stack

ClassVAR는 높은 확장성 및 가용성을 목표로 컨테이너 기반의 MSA 구조로 개발되었습니다.

현재는 Swarmprom 템플릿 이미지를 빌렸지만 확장하면서 정규 이미지로 교체할 예정입니다.

[실행 방법은 이 문서를 참고](./RUN.md)

### Load Balancing

[Traefik](https://traefik.io/) - Orchestration-aware Router

### Container Orchestration

[Docker Swarm](https://docs.docker.com/engine/swarm/)

### Service Tech-stacks

#### Typescript, ReactJs

Features:
- Frontend Pages

#### Spring Boot

Features:
- API Servers

#### SocketIO

Features:
- Client-side Recording
- Siganling Server
- Realtime Chat
- Realtime Notification

#### WebRTC ([wrtc](https://github.com/node-webrtc/node-webrtc))
- Server-side Recording (Not ready for cloud environment)

#### STUN/TURN Server

Using [coturn](https://github.com/coturn/coturn)

### CI/CD

GitHub Actions

[Docker Registry](https://hub.docker.com/)

Docker Swarm (TODO - utilizing `docker stack deploy`)
- such as [this action](https://github.com/marketplace/actions/docker-deployment)

[Netlify](https://www.netlify.com/) (frontend CI/CD)

### Monitoring

Grafana, Prometheus, Portainer