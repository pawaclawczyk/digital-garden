---
title: "SSH"
created-at: "2022-05-01 20:09"
public: true
language: en
tags: [idea]
---

# SSH

## Tips

### How to get IP address of a source host? 

List logged users.

```
who
```

List established network connection.

```bash
sudo netstat -tnpa | grep 'ESTABLISHED.*sshd'
```
