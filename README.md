# Kalikasan Camp

## Documentation

Documentation for Cocorico is available [here](doc/index.md)

### Quick Installation Based On Docker

To start the container in the background

``` bash
docker run -d --name cocorico -ti -p 80:80 -p 3306:3306 -p 9001:9001 -p 27017:27017  -v `pwd`:/cocorico -v `pwd`/tmp/mysql:/var/lib/mysql -v `pwd`/tmp/mongo:/data/db -e HOST_UID=$UID cocolabs/cocorico
```

Connect to the container and run a command

``` bash
docker exec -it --user cocorico cocorico sh
```

Stop and remove the container before restarting

``` bash    
docker stop cocorico && docker rm cocorico
```

View at [http://localhost](http://localhost) once the Symfony server is running

Control processes with Supervisor at [http://localhost:9001](http://localhost:9001)
