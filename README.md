# Project_akhir_Kelompok_A

## Path Direktori
Final_Project/
├── README.md                          # Penjelasan umum proyek
├── .gitignore                         # File/direktori yang diabaikan oleh Git
├── terraform/                         # Konfigurasi Terraform untuk provisioning infrastruktur
│   ├── main.tf                        # File utama Terraform
│   ├── variables.tf                   # Deklarasi variabel Terraform
│   ├── outputs.tf                     # Output dari infrastruktur yang dibuat
│   ├── provider.tf                    # Penyedia layanan (AWS)
│   └── modules/                       # Modul Terraform
│       ├── vpc/                       # Modul VPC (Virtual Private Cloud)
│       ├── ec2/                       # Modul untuk EC2 instances
│       ├── rds/                       # Modul untuk RDS (Relational Database Service)
│       └── s3/                        # Modul untuk S3 bucket
├── ansible/                           # Konfigurasi Ansible untuk pengelolaan server
│   ├── playbook.yml                   # Playbook utama Ansible
│   ├── inventory/                     # Inventori server
│   │   └── hosts                      # Daftar server yang digunakan
│   └── roles/                         # Role Ansible untuk otomatisasi
│       ├── docker/                    # Role untuk instalasi Docker
│       │   ├── tasks/
│       │   │   └── main.yml
│       │   └── templates/
│       └── monitoring/                # Role untuk Prometheus & Grafana
│           ├── tasks/
│           │   └── main.yml
│           └── templates/
├── app/                               # Aplikasi OpenSID
│   ├── Dockerfile                     # Dockerfile untuk backend OpenSID
│   ├── docker-compose.yml             # Konfigurasi multi-container (opsional)
│   ├── src/                           # Hanya bagian kode sumber yang relevan
│   │   ├── config/                    # Konfigurasi aplikasi
│   │   ├── database/                  # Skrip untuk migrasi database
│   │   ├── desa/                      # Data default desa
│   │   ├── system/                    # Kernel aplikasi
│   │   ├── themes/                    # Tema bawaan OpenSID
│   │   └── index.php                  # Entry point aplikasi
│   └── tests/                         # Pengujian aplikasi
│       ├── unit/                      # Unit tests
│       └── integration/               # Integration tests
├── ci-cd/                             # Konfigurasi pipeline CI/CD
│   ├── pipeline.yml                   # Pipeline untuk GitHub Actions
│   ├── buildspec.yml                  # Build script untuk CodeBuild
│   └── deploy.yml                     # Deployment script (opsional)
├── monitoring/                        # Konfigurasi monitoring
│   ├── prometheus/                    # Konfigurasi Prometheus
│   │   └── prometheus.yml
│   └── grafana/                       # Dashboard Grafana
│       ├── dashboard.json             # Dashboard untuk monitoring aplikasi
│       └── datasources.json           # Sumber data Grafana
├── docs/                              # Dokumentasi proyek
│   ├── requirements.md                # Technical Requirement Document (TRD)
│   ├── architecture-diagram.png       # Diagram arsitektur
│   ├── timeline.md                    # Timeline proyek
│   ├── usage.md                       # Panduan penggunaan aplikasi
│   └── team.md                        # Informasi anggota tim
