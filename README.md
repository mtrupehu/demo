## Push To Docker Registry Workflow
Workflow builds docker image with name `"${System.env.DOCKER_REGISTRY_URL}/${System.env.DOCKER_ORGANIZATION}/demo:@project.version"` and pushes the image
into configured docker registry.

The GitHub secrets in table below needs to be configured:

| Name | Description |
| ---- | ----------- |
| DOCKER_USERNAME | Username for Docker registry authentication. |
| DOCKER_PASSWORD | Docker registry password. |
| DOCKER_ORGANIZATION | Path to the docker image registry, e.g. for image `foo/bar/micronaut:0.1` it is `foo/bar`. |
| DOCKER_REGISTRY_URL | Docker registry url. |
### Examples of configuration
> Specifics on how to configure public cloud docker registries like DockerHub, Google Container Registry (GCR), AWS Container Registry (ECR),
> Oracle Cloud Infrastructure Registry (OCIR) and many more can be found in [docker/login-action](https://github.com/docker/login-action)
> documentation.

#### DockerHub

- `DOCKER_USERNAME` - DockerHub username
- `DOCKER_PASSWORD` - DockerHub password or personal access token
- `DOCKER_ORGANIZATION` - DockerHub organization or the username in case of personal registry
- `DOCKER_REGISTRY_URL` - No need to configure for DockerHub

> See [docker/login-action for GCR](https://github.com/docker/login-action#dockerhub)

#### Google Container Registry (GCR)
Create service account with permission to edit GCR or use predefined Storage Admin role.

- `DOCKER_USERNAME` - set exactly to `_json_key`
- `DOCKER_PASSWORD` - content of the service account json key file
- `DOCKER_ORGANIZATION` - `<project-id>`
- `DOCKER_REGISTRY_URL` - `gcr.io`

> See [docker/login-action for GCR](https://github.com/docker/login-action#google-container-registry-gcr)

#### AWS Elastic Container Registry (ECR)
Create IAM user with permission to push to ECR (or use AmazonEC2ContainerRegistryFullAccess role).

- `DOCKER_USERNAME` - access key ID
- `DOCKER_PASSWORD` - secret access key
- `DOCKER_ORGANIZATION` - no need to set
- `DOCKER_REGISTRY_URL` - set to `<aws-account-number>.dkr.ecr.<region>.amazonaws.com`

> See [docker/login-action for ECR](https://github.com/docker/login-action#aws-elastic-container-registry-ecr)

#### Oracle Infrastructure Cloud Registry (OCIR)
[Create auth token](https://www.oracle.com/webfolder/technetwork/tutorials/obe/oci/registry/index.html#GetanAuthToken) for authentication.

- `DOCKER_USERNAME` - username in format `<tenancy>/<username>`
- `DOCKER_PASSWORD` - account auth token
- `DOCKER_ORGANIZATION` - `<tenancy>/<registry>`
- `DOCKER_REGISTRY_URL` - set to `<aws-account-number>.dkr.ecr.<region>.amazonaws.com`

> See [docker/login-action for OCIR](https://github.com/docker/login-action#oci-oracle-cloud-infrastructure-registry-ocir)
## Feature tomcat-server documentation

- [Micronaut Tomcat Server documentation](https://micronaut-projects.github.io/micronaut-servlet/1.0.x/guide/index.html#tomcat)

## Feature github-workflow-docker-registry documentation

- [https://docs.github.com/en/free-pro-team@latest/actions](https://docs.github.com/en/free-pro-team@latest/actions)

## Feature elasticsearch documentation

- [Micronaut Elasticsearch Driver documentation](https://micronaut-projects.github.io/micronaut-elasticsearch/latest/guide/index.html)

## Feature openapi documentation

- [Micronaut OpenAPI Support documentation](https://micronaut-projects.github.io/micronaut-openapi/latest/guide/index.html)

- [https://www.openapis.org](https://www.openapis.org)

## Feature http-client documentation

- [Micronaut Micronaut HTTP Client documentation](https://docs.micronaut.io/latest/guide/index.html#httpClient)

## Feature tracing-jaeger documentation

- [Micronaut Jaeger Tracing documentation](https://docs.micronaut.io/latest/guide/index.html#jaeger)

- [https://www.jaegertracing.io](https://www.jaegertracing.io)

## Feature kafka-streams documentation

- [Micronaut Kafka Streams documentation](https://micronaut-projects.github.io/micronaut-kafka/latest/guide/index.html#kafkaStream)

## Feature kubernetes documentation

- [Micronaut Kubernetes Support documentation](https://micronaut-projects.github.io/micronaut-kubernetes/latest/guide/index.html)

- [https://kubernetes.io/docs/home/](https://kubernetes.io/docs/home/)

## Feature jdbc-tomcat documentation

- [Micronaut Tomcat JDBC Connection Pool documentation](https://micronaut-projects.github.io/micronaut-sql/latest/guide/index.html#jdbc)

## Feature security-ldap documentation

- [Micronaut Micronaut Security LDAP documentation](https://micronaut-projects.github.io/micronaut-security/latest/guide/index.html#ldap)

## Feature management documentation

- [Micronaut Micronaut Management documentation](https://docs.micronaut.io/latest/guide/index.html#management)

## Feature rxjava3 documentation

- [Micronaut RxJava 3 documentation](https://micronaut-projects.github.io/micronaut-rxjava3/snapshot/guide/index.html)

## Feature jmx documentation

- [Micronaut JMX endpoints documentation](https://micronaut-projects.github.io/micronaut-jmx/latest/guide/index.html)

## Feature aws-v2-sdk documentation

- [Micronaut AWS v2 SDK documentation](https://micronaut-projects.github.io/micronaut-aws/latest/guide/)

- [https://docs.aws.amazon.com/sdk-for-java/v2/developer-guide/welcome.html](https://docs.aws.amazon.com/sdk-for-java/v2/developer-guide/welcome.html)

## Feature kafka documentation

- [Micronaut Kafka Messaging documentation](https://micronaut-projects.github.io/micronaut-kafka/latest/guide/index.html)

## Feature aws-alexa documentation

- [Micronaut Alexa Skills documentation](https://micronaut-projects.github.io/micronaut-aws/latest/guide/index.html#alexa)

## Feature jackson-xml documentation

- [Micronaut Jackson XML serialization/deserialization documentation](https://micronaut-projects.github.io/micronaut-jackson-xml/latest/guide/index.html)

- [https://github.com/FasterXML/jackson-dataformat-xml](https://github.com/FasterXML/jackson-dataformat-xml)

## Feature views-thymeleaf documentation

- [Micronaut Thymeleaf views documentation](https://micronaut-projects.github.io/micronaut-views/latest/guide/index.html#thymeleaf)

- [https://www.thymeleaf.org/](https://www.thymeleaf.org/)

## Feature security-jwt documentation

- [Micronaut Micronaut Security JWT documentation](https://micronaut-projects.github.io/micronaut-security/latest/guide/index.html)

## Feature sql-jdbi documentation

- [Micronaut Jdbi documentation](https://micronaut-projects.github.io/micronaut-sql/latest/guide/index.html#jdbi)

## Feature aws-lambda documentation

- [Micronaut AWS Lambda Function documentation](https://micronaut-projects.github.io/micronaut-aws/latest/guide/index.html#lambda)

## Feature cache-caffeine documentation

- [Micronaut Caffeine Cache documentation](https://micronaut-projects.github.io/micronaut-cache/latest/guide/index.html)

- [https://github.com/ben-manes/caffeine](https://github.com/ben-manes/caffeine)

