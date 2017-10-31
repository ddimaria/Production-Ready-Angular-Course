# Creating a New Project

You can create a new project with a single command:
```shell
ng new PROJECT-NAME --style=scss
```
All files will download, and npm will begin installing packages.

Once this process is complete, simply go into the directory and serve up the skeleton app:
```shell
cd PROJECT-NAME
ng serve
```

The default host is `localhost` and the default port is `4200`.  You can view the skeleton app at:
```shell
open http://localhost:4200/
```

You can override the default host and port with command line options (`--host`, `--port`) when invoking the development server:
```shell
ng serve --host 0.0.0.0 --port 4201
```
