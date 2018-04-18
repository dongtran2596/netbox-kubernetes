# netbox-kubernetes
1. Tệp netbox-app-deployment.yaml mô tả 1 deployment có replicas = 2. Hai container được chạy trong 1 pod là netbox-nginx + netbox-app
2. Tệp netbox-db-deployment.yaml mô tả deployment database cho netbox. Container netbox-db
3. Tệp netbox-app.yaml, cấu hình dịch vụ cho netbox-app-deployment
4. Tệp netbox-db.yaml, cấu hình dịch vụ cho database
5. Tạo secret để lưu trữ thông tin bí mật (Các file được lưu trữ trong thư mục secret):
kubectl create secret generic netbox-secret --from-file=secret_key=secret/secret_key.txt --from-file=email_address=secret/email_address.txt --from-file=email_password=secret/email_password.txt --from-file=netbox_password=secret/netbox_password.txt --from-file=db_password=secret/db_password.txt --from-file=superuser_password=secret/superuser_password.txt
