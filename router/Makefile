build:
	docker build --platform linux/amd64 -f Dockerfile . -t router-amd64

push:
	docker tag router-amd64 gcr.io/summit-enterprise-workshop/jesse-apollo-router:latest
	docker push gcr.io/summit-enterprise-workshop/jesse-apollo-router:latest

deploy:
	echo "Running Google Cloud Build" && \
	gcloud builds submit --config ./cloudbuild.yaml
