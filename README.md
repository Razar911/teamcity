# Teamcity server
##### Download code to your server:

```
git clone https://github.com/Razar911/teamcity.git
```

Set TeamCity version in `.env` file

##### Run docker-compose:
```
cd teamcity/

docker-compose up -d
```

##### After start all containers, Teamcity server will be able at:

`http://localhost:8112` or `http://{YOUR_SERVER_IP}:8112`

<br>
After creating a user, visit ["Agents -> Unauthorized"] to authorize the build agent.
