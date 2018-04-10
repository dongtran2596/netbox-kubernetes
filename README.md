# netbox-kubernetes
1. Tệp netbox-app-deployment.yaml mô tả 1 deployment có replicas = 2. Hai container được chạy trong 1 pod là netbox-nginx + netbox-app
2. Tệp netbox-db-deployment.yaml mô tả deployment database cho netbox. Container netbox-db
3. Tệp netbox-app.yaml, cấu hình dịch vụ cho netbox-app-deployment
4. Tệp netbox-db.yaml, cấu hình dịch vụ cho database
