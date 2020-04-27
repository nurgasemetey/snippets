###  Efficiently delete large directory containing thousands of files


[linux - Efficiently delete large directory containing thousands of files - Unix &amp; Linux Stack Exchange](https://unix.stackexchange.com/questions/37329/efficiently-delete-large-directory-containing-thousands-of-files "linux - Efficiently delete large directory containing thousands of files - Unix &amp; Linux Stack Exchange")


 

```bash
mkdir empty_dir
rsync -a --delete empty_dir/    yourdirectory/

```
