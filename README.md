# How to use?
1. Install [Docker](https://docs.docker.com/engine/install/ubuntu/) on server
2. Install [node_exporter](https://prometheus.io/docs/guides/node-exporter/)
3. Configure targets in config/prometheus/prometheus.yml
4. Run Docker container
5. Visit YOUR-IP:3000 (admin / admin)

# What is docker-compose.exporters.yml?
I split exporters and prometheus/grafana because I needed to collect metrics from host.
But if you want collect metrics from docker, just copy all you need to docker-compose.yml.

# Easy way to install Docker
```bash
sudo apt update &&
sudo apt install ca-certificates curl gnupg lsb-release apt-transport-https software-properties-common &&
sudo mkdir -p /etc/apt/keyrings &&
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
 echo "deb [ arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null &&
sudo apt update &&
sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```


# Useful links
1. [How to install docker](https://docs.docker.com/engine/install/ubuntu/) 
2. [Prometheus](https://prometheus.io/)
3. [Grafana](https://grafana.com/)
4. [Grafana Dashboard for Node Exporter](https://grafana.com/grafana/dashboards/12486-node-exporter-full/)
5. [Fix issue with /var/lib/grafana is not writable](https://github.com/cfbarbero/tick-grafana-docker/issues/1)
