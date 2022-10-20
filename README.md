# gradle-dependencies-sorter

This JVM CLI app and companion Gradle plugin can sort the dependencies of a `build.gradle` script.

## Usage

### CLI

```shell
./path/to/sort <path(s) that contain build.gradle scripts>

# for example, use this to sort the full repo
./path/to/sort .

# for example, use this to sort a sub-tree
./path/to/sort features

# for example, use this to sort a single file
./path/to/sort my/app/build.gradle

# Check sort status
./path/to/sort -m check <paths as above>
./path/to/sort --mode check <paths as above>
```

### Gradle plugin

#### Sort it

```shell
./gradlew :my:app:sortDependencies

# Identical to the above
./gradlew :my:app:sortDependencies --mode sort
```

#### Check it

```shell
./gradlew :my:app:sortDependencies --mode check
```

## Test it

```shell
./gradlew check
```

## Build it

### Publish everything to maven local

```shell
./gradlew publishToMavenLocal
```

This will push all of this project's artifacts to `~/.m2/repository/`.

### Build zip distribution

```shell
./gradlew :app:shadowDistZip
```

This creates a zip file of the distribution at `app/build/distributions/`. This archive may be installed anywhere you 
like.

### Install CLI app

```shell
./gradlew :app:installShadowDist
```

This will install the app to `app/build/install/app-shadow/`.

## Pre-OSS Contributors
* https://github.com/autonomousapps
* https://github.com/darshanparajuli
* https://github.com/holmes
