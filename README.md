# RDMA example code

This code demonstrates how to use several typical RDMA Verbs APIs, including Send, Receive, RDMA Read and RDMA Write. After establishing a QP between client and server, the code has 4 tests.

```
Test 1: server use 'Send' operation to put 'MSG_S' into client's buffer.
Test 2: client use 'Send' operation to put 'MSG_C' into server's buffer.
Test 3: client use 'RDMA Read' operation to read server's buffer 'RDMAMSGR'.
Test 4: client use 'RDMA Write' operation to put 'RDMAMSGW' into server's buffer.
```

## Run the code

Compile:

`gcc -Wall -O2 -o RDMA_RC_example RDMA_RC_example.c -libverbs`

Client side:

`RDMA_RC_example -g <gid_idx> -d <ib-dev> <server_ip>`

Server side:

`RDMA_RC_example -g <gid_idx> -d <ib-dev>`
