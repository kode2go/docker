# Setup

Assuming you created a folder for your project, `cd` to the folder and copy the `Dockerfile` and `requirements.txt` file in there.

Then:

```
sudo docker build -t dj2 .
```

Run it:

```
sudo docker run -p 8000:8000 dj2
```

Open it:

```
http://localhost:8000/
```

![image](https://github.com/kode2go/docker/assets/29664888/ec9eedef-2ffb-4625-bcc0-4e1fbd188e5e)
