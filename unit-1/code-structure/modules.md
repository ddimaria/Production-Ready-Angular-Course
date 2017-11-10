# Modules

## Root Module
* By design, Angular is a modular system.  
* After installing via the CLI, a single app.module (AppModule) is installed.  This is referred to as the `Root Module`.  
* You need at least one module class in Angular.
* For small to medium sized applications, this Root Module may be all you need.
* Services added to modules in the `providers` array can act as singletons when injected to child components.  Providers added to the Room Module are called `Application Scoped Providers`.

## Feature Modules
* As you application grows, the developer can start organizing the application into multiple, feature modules, which extends the application.
* The Root Module will then be the containing/parent the Feature Modules.
* Feature Modules go into the `imports` section of the containing module.
* Feature Modules can be thought of as self-contained, mini applications, though there's nothing stopping the developer from coupling to other modules, which may sometimes be desired.
* A Feature Module can hide it's components, directives, and pipes by `not` exporting them.
* It's possible to go overboard with modules, which can cause a bit of configuration duplication.
* Feature Modules can be used to resolve conflicts in directives/components by scoping them to the individual modules.


### When do you use Feature Modules?
* Component/Direct scope isolation is desired.
* There is a clear separation in business domain.
* There is a different user workflow (e.g. admin vs user-facing).
* Utilities have enough in common to be separated out.
* The application grows in complexity with a single Root Module.
* Lazy module loading is desired for loading performance.

## Shared Modules
* Modules are typically decoupled from other modules (sans parent-child models).
* Shared Modules are desired for common components, directives, and pipes that can be used in many parts of the applicaiton.
* Sharing Modules can avoid instance duplications.
* They export and re-export components, directives, and pipes.
* Application wide, singleton service providers in a shared module that are imported by a lazy-loaded module makes its own copy of the service.
