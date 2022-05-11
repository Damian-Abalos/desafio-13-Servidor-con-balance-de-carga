para levantar la base de datos por consola: mongod --dbpath miBaseMongo
----------------------------------------------------------------------
para iniciar servidor con nodemon en modo FORK: nodemon server.js --p 8080 --m fork
para iniciar servidor con nodemon en modo CLUSTER: nodemon server.js --p 8080 --m cluster

para iniciar servidor con FOREVER en modo FORK: forever start server.js --p 8080 --m fork
para iniciar servidor con FOREVER en modo CLUSTER: forever start server.js --p 8080 --m cluster
para listar los datos de los procesos en ejecucion con forever: forever list

para iniciar servidor con PM2 modo fork: pm2 start server.js --name="server1" --watch -- 8080
para iniciar servidor con PM2 modo cluster: pm2 start server.js --name="server1" --watch -i max -- 8080
para listar procesos con PM2: pm2 list

para listar todos los procesos de node.js activos por sistema operativo :tasklist /fi "imagename eq node.exe"

balancear servidor de carga con PM2:

pm2 start server.js --name="server1" --watch -- 8080
pm2 start server.js --name="server2" --watch -- 8082
pm2 start server.js --name="server3" --watch -- 8083
pm2 start server.js --name="server4" --watch -- 8084
pm2 start server.js --name="server5" --watch -- 8085

luego ejecutar nginx.exe (cambiando el archivo de configuracion nginx.conf)

localhost/api/randoms