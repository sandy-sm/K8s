
### Commands and Arguments

In docker two instructions are used namely ENTRYPOINT and CMD

> ENTRYPOINT [java] [-jar] [application.jar]

Is the first instruction getting executed when docker run command is executed

If, we want to pass and command line argument we do so by,

> CMD ["-D", "server-port=8779"]


`command field in k8s overrides ENTRYPOINT`

`args field in k8s overrides CMD`



