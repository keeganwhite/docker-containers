# Traefik Container Management 
The easiest way to run this code is by creating an iNethi environment, so you have the necessary architecture in place
to use this code. Find a GUI builder for iNethi [here](https://github.com/iNethi/gui-installer).

## Prerequisites
1. Traefik running
2. Keycloak running
3. A keycloak client running matching your docker-compose environment variables. You can import the maintain.json file 
into keycloak that is located [here](./maintain.json).

## Running the code
Run the docker-compose.yml file once you have edited the environment/argument variables that will be parsed at build
time:
```
docker-compose up -d
```
### Variable details
**keegan337/traefik-container-manager**:
- **HOST_IP**: the IP address of the server that containers will be installed on.
**keegan337/traefik-container-manager-frontend**:
- **REACT_APP_API_URL**: the URL of your `keegan337/traefik-container-manage` API.
- **REACT_APP_KEYCLOAK_AUTH_URL**: your keycloak auth URL.
- **REACT_APP_REALM**: the realm your keycloak client is in.
- **REACT_APP_CLIENTID**: the client ID for you `keegan337/traefik-container-manager-frontend`
