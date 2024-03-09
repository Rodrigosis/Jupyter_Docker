docker build --tag=desenvolvimento:python .
docker create -t -i --name python-dev -p 4000:4000 -v C:\Users\RODRIGO\notebooks:/home/user desenvolvimento:python
docker start python-dev
docker exec -it python-dev bash
jupyter notebook --ip 0.0.0.0 --port 4000 --allow-root
