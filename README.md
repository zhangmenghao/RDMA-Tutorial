# RDMA example code

This code demonstrates how to use different RDMA Verbs API.

## Run the code

Compile:

`gcc -Wall -O2 -o RDMA_RC_example RDMA_RC_example.c -libverbs`

Client side:

`RDMA_RC_example -g <gid_idx> <server_ip>`

Server side:

`RDMA_RC_example -g <gid_idx>`
