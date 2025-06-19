cd my-app
ng build


docker run --rm -v ${PWD}:/work -w /work cgr.dev/chainguard/apko build nginx-base.yaml apko-nginx:test apko-nginx.tar
docker load -i .\apko-nginx.tar


docker build . -t my-app:distro
docker run -p 8080:80 --rm my-app:distro