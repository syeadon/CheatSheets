# Bash

## Move / Rename folders
    mv foo bar

You can use full path too:

    mv /home/vivek/oldfolder /home/vivek/newfolder

## GPG

Import public key of someone

```bash
gpg --import some-one.key
```

See all imported public keys

```bash
gpg --list-keys
```

Encrypt a file

```bash
gpg --encrypt --armor -r some-one@server.com file.txt
```

## PDF

Count the words of a PDF file:

```bash
pdftotext myfile.pdf - | wc -w
```

## Aliases

Load fork from the current directory

	echo alias ll="/C/Users/syeadon/AppData/Local/Fork/Fork.exe '$(pwd -W)'" >> .bashrc