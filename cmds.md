## creating express-server
`
docker run -d -p 8080:8080 --name express-server manojpandekamat/express-server

`

## creating a generator

`
docker run -itd  -e SERVER_URL="http://10.1.21.11:8000/predict" -e THREAD_COUNT=10 manojpandekamat/loadgenerator

`

# creating a mri-app


`
 docker run -d -p 8000:8000 -v "/c/Users/Manoj/AI Libraries/DL/MinorProject/data:/data"  manojpandekamat/fastapi-api-metrics1

`

timestamp,current_requests,cpu_percent,memory_percent,disk_read_bytes,disk_write_bytes,net_bytes_sent,net_bytes_recv,num_threads,open_files


Running node app
`
docker run -itd -p 8000:8000 --name edge-node1 -e REMOTE_SERVER_URL="http://192.168.126.144:8080/data" manojpandekamat/fastapi-application
 docker run -itd -p 8003:8000 --name cloud-node1 -e REMOTE_SERVER_URL="http://10.1.7.221:8080/data" manojpandekamat/fastapi-applicaiton2
`

`
curl.exe -X POST "http://192.168.126.144:8000/predict" -F "file=@img.jpeg"

`
docker run -itd --env-file .env -p 5001:5001 --name schedular  manojpandekamat/schedular6