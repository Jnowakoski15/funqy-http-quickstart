Quarkus guide: https://quarkus.io/guides/funqy-http
# funqy-http-quickstart


# Building a native executable for Podman
./mvnw package -Pnative -Dquarkus.native.container-build=true -Dquarkus.native.container-runtime=podman


# Building the container image with Podman
podman build -f src/main/docker/Dockerfile.native -t funqy-http-quickstart .

# Local Running:
podman run -i --rm -p 8080:8080 funqy-http-quickstart

# Red Hat Docs:
https://access.redhat.com/documentation/en-us/red_hat_build_of_quarkus/quarkus-2-2-5/guide/438bff3e-a786-4420-b555-4639f5b8de7b#_05a5c26c-a959-4658-96ab-7894280acfe8