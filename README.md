# Elk for Docker Container Logging
This is a docker stack for local ELK logging of all docker container using **logspout**.
## Setup
- Clone repo and go to folder.
- Copy `.env.example` to `.env` and change password.

- Run:
```
docker-compose up -d
```

- After the service starts, open Kibana in a browser at: 
```
http://localhost:5601
```

User: `elastic`  
Password: from `.env` file.

- On the ***Home*** page in Kibana, click on the: ***Connect to your Elasticsearch Index*** link on the right side.
- Create an index pattern, add `logstash-*` and click ***Next***.
- On the next page select `@timestamp` as the ***time filter field name***. Then click ***Create Index Pattern***

After that you are set up! Go to the ***Discover*** page and start looking at logs!

## Documentation

https://github.com/looplab/logspout-logstash
