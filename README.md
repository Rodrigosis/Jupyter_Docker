docker build --tag=jupyter_docker:latest .
docker create -t -i --name experiments -p 4000:4000 -v C:\Users\RODRIGO\notebooks:/home/user jupyter_docker:latest
docker start experiments
docker exec -it experiments bash
jupyter notebook --ip 0.0.0.0 --port 4000 --allow-root
