# dirtyfrag
Linux kernel LPE. Chains two page-cache write bugs in `esp4`/`esp6`/`rxrpc` to corrupt pages the kernel shouldn't be writing to, giving any local user instant root. No race condition needed, very reliable. Descendant of Dirty Pipe and Copy Fail.
