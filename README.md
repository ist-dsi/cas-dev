# CAS Development Docker Image
=====

**DISCLAIMER - This is a DEVELOPMENT container, not to be used in production.**

To run this docker image, you should do the following:

1. Update the people.txt file in the config folder to have your users in the following format:
	
	``` username::password ```

2. Run the docker container using the following command: 

	```
	docker run --name cas \
		-p 8080:8080 \
		-p 8443:8443 \
		-v $(pwd)/config:/config \
		istdsi/cas-dev
	```

3. Use the following login url:

	``` https://localhost:8443/cas/login?service=<your-service-callback-url> ```