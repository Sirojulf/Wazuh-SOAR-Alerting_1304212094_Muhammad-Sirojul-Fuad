# Wazuh SOAR Alerting (FIM, Failed Login, Agent Disconnected)

### Prasyarat
- **Docker Engine** + **Docker Compose plugin** (cek: `docker compose version`)
- Disarankan RAM **≥ 6–8 GB** (OpenSearch cukup berat)

### 1) Clone repo 
```bash
git clone https://github.com/<username>/wazuh-soar-alerting.git
cd wazuh-soar-alerting
```

### 2) Jalankan Wazuh Stack (Single Node) pakai Docker


```bash
git clone https://github.com/wazuh/wazuh-docker.git

cd wazuh-docker/single-node

docker compose up -d
```

Cek status container:
```bash
docker compose ps
```

Lihat log:
```bash
docker compose logs -f
```

### 3) Akses Wazuh Dashboards
 Buka di browser: `https://localhost`


### 4) Stop  (opsional)
Stop:
```bash
docker compose down
```



## Struktur folder 
```
├─ dataset/
│ └─ events-2025-12-14T14_54_18.563Z.csv
├─ monitors/
│ ├─ agent_disconnected_monitor.json
│ ├─ failed_login_monitor.json
│ └─ fim_syscheck_monitor.json
├─ paper/
│ ├─ Article_SOAR_Tech.pdf
│ └─ Tugas review paper individu_Muhammad Sirojul Fuad_1304212094.pdf
├─ report/
│ ├─ Laporan_Implementasi_SOAR_Wazuh_FIM_FailedLogin_Disconnect.docx
│ ├─ Laporan_Implementasi_SOAR_Wazuh.pdf
│ └─ wazuh report.pdf
├─ templates/
│ ├─ slack_agent_disconnected.mustache
│ ├─ slack_failed_login.mustache
│ └─ slack_fim.mustache
└─ README.md
```

## dataset
Berisi data hasil export event/log dari Wazuh

## monitors
Berisi file konfigurasi monitor Alerting (OpenSearch Dashboards) dalam format JSON.

## report
Berisi laporan hasil implementasi

## templates
Berisi template pesan Slack 
## Link repo
- GitHub: https://github.com/Sirojulf/Wazuh-SOAR-Alerting_1304212094_Muhammad-Sirojul-Fuad
