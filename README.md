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
sudo apt-get update &&
sudo apt-get install ca-certificates curl gnupg lsb-release &&
sudo mkdir -p /etc/apt/keyrings &&
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
 echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null &&
sudo apt-get update &&
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin &&
sudo curl -L "https://github.com/docker/compose/releases/download/v2.10.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose && sudo chmod +x /usr/local/bin/docker-compose
```

# Useful links
1. [How to install docker](https://docs.docker.com/engine/install/ubuntu/) 
2. [Prometheus](https://prometheus.io/)
3. [Grafana](https://grafana.com/)
4. [Grafana Dashboard for Node Exporter](https://grafana.com/grafana/dashboards/12486-node-exporter-full/)
5. [Fix issue with /var/lib/grafana is not writable](https://github.com/cfbarbero/tick-grafana-docker/issues/1)