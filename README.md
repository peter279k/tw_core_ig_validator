# tw_core_ig_validator

- It's the offline for [Taiwan Core IG validator](https://twcore.mohw.gov.tw/ig/twcore) Docker image.
- The Taiwan Core IG includes [CI Build](https://twcore.mohw.gov.tw/ig/twcore) and [MOHW](https://twcore.mohw.gov.tw/ig/twcore).

- The Docker image with the specific TW Core IG version and OpenJDK 11 is available on the [Docker hub](https://hub.docker.com/repository/docker/peter279k/tw_core_ig_validator_11).
- The Docker image with the specific TW Core IG version and OpenJDK 17 is available on the [Docker hub](https://hub.docker.com/repository/docker/peter279k/tw_core_ig_validator_17).

# Usage

- If you prefer the JDK 11 with the TW Core IG 0.2.2 version, please run the following command:

```sh
docker pull peter279k/tw_core_ig_validator_11:0.2.2
```

- If you prefer JDK 17 with the TW Core 0.2.2 IG 0.2.2 verison, please run the following command:

```sh
docker pull peter279k/tw_core_ig_validator_17:0.2.2
```

- If you prefer the JDK 11 with the latest TW Core IG version, please run the following command:

```sh
docker pull peter279k/tw_core_ig_validator_11:latest
```

- If you prefer JDK 17 with the latest TW Core IG verison, please run the following command:

```sh
docker pull peter279k/tw_core_ig_validator_17:latest
```

# Run Validator Usage

```sh
docker run \
    -v /path/to/resource.json:/root/resource.json \
    peter279k/tw_core_ig_validator_11:0.2.2 \
    -c "cd /root/ && java -Dfile.encoding=UTF-8 -jar validator_cli.jar ./resource.json -version 4.0 -ig tw.gov.mohw.twcore"
```
