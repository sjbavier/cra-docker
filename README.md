# Create-react-app storybook yarn and sass development in Docker

This was created from [https://start.jcolemorrison.com/no-eject-create-react-app-with-sass-storybook-and-yarn-in-a-docker-environment/] 

Build the images

```sh
docker build -t <docker-user>/cra-storybook-dev ./cra-yarn-storybook
docker build -t <docker-user>/sass-dev ./sass-dev
```

Run create-react-app and getstorybook

```sh
# build the cra
docker-compose -f ../cmd.yml run web create-react-app .
# set up react storybook
docker-compose -f ../cmd.yml run web getstorybook .
```

Run the containers

```sh
# run in detached mode
docker-compose up -d
```