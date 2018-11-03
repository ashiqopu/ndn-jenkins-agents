### Homebrew
Homebrew breaks when cleaned and reinstalled as owner permissions are not given. A workaround is to explicitly create the relevant directories and ```sudo chown``` them as below:
```
sudo mkdir -p /usr/local/bin /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/var /usr/local/opt /usr/local/share /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
```

```
sudo chown -R jenkins:jenkins /usr/local/bin /usr/local/include /usr/local/lib /usr/local/sbin /usr/local/var /usr/local/opt /usr/local/share /usr/local/Cellar /usr/local/Caskroom /usr/local/Homebrew /usr/local/Frameworks
```

Workaround discussion is [here](https://github.com/Homebrew/brew/issues/4997). Take a look at [this](https://github.com/Homebrew/brew/issues/4997#issuecomment-425771026) comment.
