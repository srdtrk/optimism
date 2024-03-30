### Hola amigo!

Some small things for running e2e's (and some minor pitfalls):

First, add the binary, build and copy in this directory:

```bash
make build-interceptor
```

After copying to `interceptor-node` folder, can just invoke a specific e2e with:

```bash
go test -v -run TestDepositTxCreateContract ./...
```

---

In this dir:

- `interceptor.go` calls our interceptor binary (which will invoke peptide binary).
- `client.go` holds a tiny rpc client we can use to interact with interceptor-node rpc server.
