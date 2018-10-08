# compile
# on windows

docker-machine create -d "virtualbox" --virtualbox-memory "1024" --virtualbox-hostonly-cidr "192.168.99.101/24" --virtualbox-share-folder "E:\MyProjects\compilebox:app" compiler
docker build -t 'virtual_machine' .
cd API
npm i
node app.js