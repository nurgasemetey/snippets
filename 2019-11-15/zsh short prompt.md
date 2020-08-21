###  zsh short prompt


[shell - Shortening my prompt in Zsh - Stack Overflow](https://stackoverflow.com/questions/37286971/shortening-my-prompt-in-zsh "shell - Shortening my prompt in Zsh - Stack Overflow")


 

```shell
Old question, I know, but as an alternative solution I just discovered powerlevel9k, an extension of agnoster (they appear practically identical bar a fair few tweaks), which has this functionality built in.

Just set it as your zsh theme, then in .zshrc set

POWERLEVEL9K_SHORTEN_DIR_LENGTH=2

which ensures that only two directories are listed.

Alternate options are outlined in the readme.
```
