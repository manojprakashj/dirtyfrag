# dirtyfrag
Linux kernel LPE. Chains two page-cache write bugs in `esp4`/`esp6`/`rxrpc` to corrupt pages the kernel shouldn't be writing to, giving any local user instant root. No race condition needed, very reliable. Descendant of Dirty Pipe and Copy Fail.


<img width="900" height="470" alt="linux" src="https://github.com/user-attachments/assets/58699f41-42c9-4307-bc3b-d41d31e8727d" />
