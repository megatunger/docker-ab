# docker-ab

Run Apache benchmark tool (ab) from container and visualize results.

## Usage
Install Docker. Clone this repo to your local machine. Run docker-compose: 
```bash
docker-compose up
```

### Connect to ab container:
```bash
docker-compose exec ab sh
```

### Run ab:
```bash
cat /mnt/urls/urls | parallel --colsep ',' "ab -e {2} -c 2 -n 200 {1} && cat {2} | tail -n 100 | sed 's/^/{2},/' >> /tmp/ab.csv"
```

### Open Kibana webinterface
```bash
http://localhost:5601/
```

![ab](ab.png?raw=true)
