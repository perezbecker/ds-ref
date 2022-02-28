# bash

## sudo cat

__issue:__ `sudo cat input1.txt input2.txt > output.txt` gives a permission denied. 

The problem is that the redirection is being processed by your original shell, not by sudo. Shells are not capable of reading minds and do not know that that particular >> is meant for the sudo and not for it.

You need to:

- quote the redirection (so it is passed on to `sudo`)
- and use `sudo -s` (so that sudo uses a shell to process the quoted redirection.)

```bash
sudo bash -c 'cat input1.txt input2.txt > output.txt'
sudo -s 'cat input1.txt input2.txt > output.txt'
```