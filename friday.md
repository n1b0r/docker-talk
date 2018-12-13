
# Swarmprom

Swarmprom is a starter kit for Docker Swarm monitoring with Prometheus, Grafana, cAdvisor, Node Exporter, Alert Manager and Unsee.

 * prometheus (metrics database) http://<swarm-ip>:9090
 * grafana (visualize metrics) http://<swarm-ip>:3000
 * node-exporter (host metrics collector)
 * cadvisor (containers metrics collector)
 * dockerd-exporter (Docker daemon metrics collector, requires Docker experimental metrics-addr to be enabled)
 * alertmanager (alerts dispatcher) http://<swarm-ip>:9093
 * unsee (alert manager dashboard) http://<swarm-ip>:9094
 * caddy (reverse proxy and basic auth provider for prometheus, alertmanager and unsee)

Veuillez suivre les instructions données dans le readme du projet : [https://github.com/stefanprodan/swarmprom](https://github.com/stefanprodan/swarmprom)

Veuillez utiliser la commande suivante pour déployer la stack (valide sous linux et windows):

```
docker stack deploy -c docker-compose.yml mon
```

Utilisez la stack `friendlyhello` (web python + redis) pour tester les différents composants vous permettant de monitorer efficacement vos stacks docker swarm.

Bonus : mettez en place de l'alerting via Slack

# Docker for developers !

Par binome ou par groupe sur une technologie de votre choix, vous devez dockeriser une application. 

Pour cela vous devrez :
  - créer un Dockerfile
  - construire une image
  - utiliser docker-compose pour vous créer un environment de test (web + base de donnée par exemple)

# Docker official workshop

Pour les développeurs les plus aguerris voici le workshop de Bret Fisher (monsieur docker captain 2018) : https://dockercon18eu.bretfisher.com

Vous n'aurez pas accès à des instances aws pour effectuer les tests. Veuillez utiliser votre machine ou la plateforme [playwithdocker](https://labs.play-with-docker.com/)

Good luck !
