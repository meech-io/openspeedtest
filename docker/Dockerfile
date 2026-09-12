# meech-io/openspeedtest: stock OpenSpeedTest server image with a multi-origin client.
# Build:  docker build -t openspeedtest-multi -f docker/Dockerfile .
# Run:    docker run -d --restart unless-stopped --name openspeedtest \
#           -p 80:3000 -p 443:3001 -p 8081:3002 -p 8082:3003 -p 8083:3004 openspeedtest-multi
FROM openspeedtest/latest:latest

COPY docker/OpenSpeedTest-Server.conf /etc/nginx/conf.d/OpenSpeedTest-Server.conf
COPY index.html hosted.html /usr/share/nginx/html/
COPY assets /usr/share/nginx/html/assets

EXPOSE 3000 3001 3002 3003 3004
