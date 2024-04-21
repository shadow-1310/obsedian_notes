using virtual env in jupyter 
[gfg post](https://www.geeksforgeeks.org/using-jupyter-notebook-in-virtual-environment/)
[medium post](https://towardsdatascience.com/run-a-new-jupyter-notebook-in-an-already-existing-virtual-environment-7490b3dd5ab6)

```bash
pip install ipykernel
```

## create a new environment
```bash
ipython kernel install --user --name=bert
```

- here bert is the environment name

## Some usefull commands

To see the running notebooks
```bash
jupyter server list
```

To stop a running notebook
```bash
jupyter notebook stop 8080
```

#### To use remote jupyter notebook
https://stackoverflow.com/questions/69244218/how-to-run-a-jupyter-notebook-through-a-remote-server-on-local-machine
- in your remote machine run
```bash
jupyter notebook --no-browser --port=8080
```

- in your local machine setup a tunnel
```bash
ssh -L 8080:localhost:8080 <REMOTE_USER>@<REMOTE_HOST>
```

- then in your browser http://localhost:8080/
- if asked for token use the following command in remote machine to see the token of the server
```bash
jupyter server list
```