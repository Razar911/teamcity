# Teamcity server
##### Download code to your server:

```
git clone https://github.com/Razar911/teamcity.git
```

Set TeamCity version, database user and password in `.env` file

Some folders:
* ./buildserver_pgdata - Posgres DB data
* ./data_dir - TeamCity data directory
* ./teamcity-server-logs - logs of primary TeamCity server
* ./agents/agent-1/conf - configuration directory for the first build agent
* ./agents/agent-min/conf - configuration directory for the minimal build agent

##### Run docker-compose:
```
cd teamcity/

docker-compose up -d
```

##### After start all containers, Teamcity server will be able at:

`http://localhost:8112` or `http://{YOUR_SERVER_IP}:8112`

<br>
After creating a user, visit ["Agents -> Unauthorized"] to authorize the build agent.

### My configuration:

My Teamcity server able at [http://94.130.17.105:8112/](http://94.130.17.105:8112/)

I create CI for my test project `https://github.com/Razar911/flatris_test`

I setup two steps:
* build image from [Dockerfile](https://github.com/Razar911/flatris_test/blob/0a065640107ebb4e82c73e5b3f23d2890c723a39/Dockerfile)
* push image to my [Dockerhub](https://hub.docker.com/repository/docker/dockerbarabash/flatris-test/general), tag `latest`

As a bonus, I added third step - Run App on Server. Application able at [http://94.130.17.105:3000/](http://94.130.17.105:3000/)
