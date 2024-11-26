# MyChatBot

This is a local chatbot that you can run on your own machine, download a model or two and start chatting.

## Setting Up

The only pre-requisite is to install Docker and Docker Compose :whale: 

### For AMD GPU

The image of ollama relies and uses a different tag for AMD GPU specifically:

```shell
ollama/ollama:rocm
```

### For CPU only

Use the tag `:latest` if you are running without a GPU

```shell
ollama/ollama:latest
```

### For NVidia GPU

Need to add a new data parameter in the `docker-compose.yml` to get all GPUs.

```yaml
...
data:
  - gpus=all
```

Run the following command to get it started:

```shell
docker compose up -d
```

Refer to the [official ollama docs](https://github.com/ollama/ollama/blob/52bbad12f96e84f7d62c5dfdd7dbba2b10b37344/docs/docker.md) for more info

Then navigate to http://localhost:8080 (feel free to change the port for the openwebui in `docker-compose.yml` if 8080 is taken)

## Experimented with CPU only

If you're curious about how it works with only a CPU, you can read the experience here: https://buymeacoffee.com/qoyyuum/how-i-made-ai-system-admin-assistant

TL;DR Get a GPU

