# Paths
You can define a folder structure when generating code.  Additionally, the CLI is aware of the directory that you are currently within and uses relative path generation.  The following are functionally equivalent and generate a component within `src/app/FEATURE/COMPONENT-NAME`:

```shell
ng g component FEATURE/COMPONENT-NAME
```
```shell
cd FEATURE
ng g component COMPONENT-NAME
```

```shell
cd ANOTHER-FEATURE
ng g component ../FEATURE/COMPONENT-NAME
```