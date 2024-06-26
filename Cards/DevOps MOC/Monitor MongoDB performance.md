## with [[Datadog Agent]] (Amazon Linux)

- Tạo MongoDB user cho Datadog Agent với client roles [read](https://www.mongodb.com/docs/manual/reference/built-in-roles/#mongodb-authrole-read) và [clusterMonitor](https://www.mongodb.com/docs/manual/reference/built-in-roles/#mongodb-authrole-clusterMonitor). Đối với [[Replica set]], login vào [[Primary]]:
	```
	# Create the user for the Datadog Agent. 
	  db.createUser({
		  "user": "datadog",
		  "pwd": "<YOUR PASSWORD>",
		  "roles": [
			  { role: "read", db: "admin" },
			  { role: "clusterMonitor", db: "admin" },
			  { role: "read", db: "local" } 
		  ]
	  })
	```
- [[Datadog Agent#Cài đặt Datadog Agent trên Amazon Linux]] trên tất cả các host thuộc MongoDB replica set và thiết lập Agent connect tới [[replica]] trên host đó. *(Chạy Agent trên từng host giúp giảm độ trễ , tăng tốc độ xử lý và duy trì data kể cả khi host xảy ra lỗi)*
  Duplicate file `/etc/datadog-agent/conf.d/mongo.d/conf.yaml.example` và đổi tên thành `conf.yaml`, cập nhật các dòng dưới đây:
    ```
    init_config:
    instances:
      - host:
	      - localhost:27017
	    username: datadog
	    password: <YOUR PASSWORD>
	    database: admin
    ```

- Thiết lập hostname hiển thị trên nền tảng Datadog bằng cách cập nhật trong file `/etc/datadog-agent/datadog.yaml`:
  ```
  hostname: <YOUR MONGODB REPLICA HOSTNAME>
  ```
- Restart Datadog Agent.
- Kiểm tra xem host đã được monitor bởi Datadog hay chưa sau khi Agent hoạt động:
	- Truy cập vào platform Datadog.
	- Ở thanh điều hướng bên trái, mở tab Infrastructure
	- Chọn Infrastructure List, tìm hostname
	  ![[datadog-infrastructure-list.png]]