# ReDex Docker Container 
[![Docker Pulls](https://img.shields.io/docker/pulls/cortinico/redex.svg)](https://hub.docker.com/r/cortinico/redex/) [![Docker Stars](https://img.shields.io/docker/stars/cortinico/redex.svg)](https://hub.docker.com/r/cortinico/redex/) 
[![](https://images.microbadger.com/badges/image/cortinico/redex.svg)](https://microbadger.com/images/cortinico/redex "Get your own image badge on microbadger.com")

![Redex+Docker](http://i.imgur.com/5CnDpdA.png)

Dockerfile for [Facebook ReDex](http://fbredex.com/) ([source](https://github.com/facebook/redex)), the Facebook Android Bytecode optimizer. If you want to better understand what does ReDex perform on your apk, let's have a look at this article: [Open-sourcing ReDex](https://code.facebook.com/posts/998080480282805/open-sourcing-redex-making-android-apps-smaller-and-faster/).

You can use this container to optimize your Android APKs without _violating_ your host system with tons of dependencies :)

## Usage

You can run ReDex with a single command
```bash
docker run -v /your-apk-folder:/data/redex cortinico/redex redex your-apk.apk -o out.apk
```
You will find a compressed apk called *out.apk* inside `/your-apk-folder` (change with your own apk folder).

## Build the container

If you want to re-build the container, you have to clone the repo and trigger the building:
```bash
git clone https://github.com/cortinico/docker-redex.git && cd docker-redex && docker build .
```

## License

The following software is licensed under the [MIT License](https://raw.githubusercontent.com/cortinico/docker-redex/master/LICENSE). Redex is license under the [BSD License](https://raw.githubusercontent.com/facebook/redex/master/LICENSE)
