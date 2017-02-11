### Docker Image for LAMP Stack

Docker image for LAMP stack, containing minimal PHP extensions


Run following code to build image
```
docker build -t lamp_stack .
```

After building image run following command to run container
``` 
docker run --name your_lamp_stack_project_name -d -v path/to/your/project/directory:/var/www/html -t -p 8080:80 lamp_stack
```

if **8080** port not available use any other available port

While *your_lamp_stack_project_name* container is running, run following code to ssh into container
```
docker exec -i -t your_lamp_stack_project_name /bin/bash
```

If *your_lamp_stack_project_name* container is not running, run following command to start it
```
docker start your_lamp_stack_project_name
```