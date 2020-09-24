<h1 align="center">
    <img src="http://docs.cocorico.io/images/logo_cocorico_20.png" alt="Cocorico"/>
</h1>

# Cocorico

## Documentation

Documentation is available [here](doc/index.md)

### Quick Installation Based On Docker

To start the container in the background

``` bash
docker run -d --name cocorico -ti -p 80:80 -p 3306:3306 -p 9001:9001 -p 27017:27017  -v `pwd`:/cocorico -v `pwd`/tmp/mysql:/var/lib/mysql -v `pwd`/tmp/mongo:/data/db -e HOST_UID=$UID cocolabs/cocorico
```

To connect to the container

``` bash
docker exec -it --user cocorico cocorico sh
```

To stop and remove the container

``` bash    
docker kill cocorico && docker rm cocorico
```

Once the Symfony server is running, enjoy Cocorico at [http://localhost](http://localhost)

Control processes with Supervisor at [http://localhost:9001](http://localhost:9001)

## License

Cocorico is released under the [MIT license](LICENSE).

## About Us

Cocorico is a creation of [Cocolabs](https://www.cocolabs.com/en/?utm_source=github&utm_medium=cocorico-page&utm_campaign=organic) specialist of online services sales solutions.
