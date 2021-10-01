# quarkus-with-vue

Simple starter template for Quarkus and Vue 3, playing around with :

- [x] Quarkus as http server
- [x] Quarkus as backend server (combined API and BFF)
- [x] Vue 3 using "CDN" (using WebJars)
- [ ] Testing Vue 3 Single File Components
- [ ] Testing Vue 3 Component Composition
- [ ] Extending with Vuetify (when it supports Vue 3)

## How to test ...

Start the Quarkus app and go to [localhost:8080](http://localhost:8080/).
Open developer console in your browser and see output in JavaScript console for test and debug output.


## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/quarkus-with-vue-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.html.
