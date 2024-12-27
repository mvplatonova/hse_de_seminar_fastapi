## TODO service
Task management service based on FastAPI

#### Add new task
POST request to http://\<host\>:\<port\>/items
<img width="1387" alt="image" src="https://github.com/user-attachments/assets/4ca0fb57-1301-4a91-aa35-cb16617b561e" />

#### Update task
PUT request to http://\<host\>:\<port\>/items/\<task_id\>
<img width="1377" alt="image" src="https://github.com/user-attachments/assets/ede47019-6ace-4f69-9b45-a40bc59bcdaf" />

#### Get task list
GET request to http://\<host\>:\<port\>/items
<img width="1370" alt="image" src="https://github.com/user-attachments/assets/cfe32bad-34c6-4f16-9440-262dcdf53489" />

#### Get task by id
GET request to http://\<host\>:\<port\>/items/\<task_id\>
<img width="1369" alt="image" src="https://github.com/user-attachments/assets/d9ee82e2-ee1c-45d2-90db-e6a724ec9ac9" />

#### Delete task by id
DELETE request to http://\<host\>:\<port\>/items/\<task_id\>
<img width="1374" alt="image" src="https://github.com/user-attachments/assets/0af889c0-cc33-4d9b-b128-1835887b19ef" />


## Short URL service
URL shortening service based on FastAPI

#### Get shorten URL
POST request to http://\<host\>:\<port\>/shorten
<img width="1371" alt="image" src="https://github.com/user-attachments/assets/c0e1af92-5ea7-49ce-a25d-ee8ed899d81a" />

#### Get info by shorten URL
Get request to http://\<host\>:\<port\>/stats/\<short_id\>
<img width="1370" alt="image" src="https://github.com/user-attachments/assets/c8ec394b-c5bc-490d-b2ab-677b4f74e581" />

#### Redirect to full URL
Go to http://\<host\>:\<port\>/\<short_id\>
<img width="1432" alt="image" src="https://github.com/user-attachments/assets/e7576d71-06ac-42cc-acfd-8857cc084ed9" />

## Launch
#### Local launch
Requirements: git, Python 3.9+

1. Clone project `git clone https://github.com/mvplatonova/hse_de_seminar_fastapi.git`
2. Go to source code folder `cd hse_de_seminar_fastapi/<service-name>`
3. Install requirements `pip install -r requirements.txt`
4. Build image `docker build -t <username>/<service_image_name> .`
5. Run service `docker run -d -p 8000:80 -v <app_name>_data:/app/data <username>/<service_image_name>`


#### Launch image from DockerHub
1. TODO service: `docker run -d -p 8000:80 -v todo_app_data:/app/data mvplatonova/service-todo-app:latest`
2. Short URL service: `docker run -d -p 8000:80 -v shorturl_app_data:/app/data mvplatonova/service_shorturl_app:latest`
