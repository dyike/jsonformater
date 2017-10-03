# jf —— Json Formater, to get pretty printer.

## How to install ?

```bash
git clone 
go get github.com/urfave/cli
cd {project dir}
go build -o jf 
sudo install ./jf /usr/local/bin/
```

OR (I have gox for some plateforms!)

```bash
sudo install ./bin/jsonformater_{best_for_you} /usr/local/bin/
```

## How to use with jf ?

### First

You can use shell `jf -h` to look for some help.

```
NAME:
   jf - Beautify json formater.

USAGE:
   jf [global options] [arg]

VERSION:
   0.1.1

AUTHOR:
   ityike <yuanfeng634@gmail.com>

COMMANDS:
     help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --input value, -i value   jf from files
   --output value, -o value  jf to files
   --help, -h                show help
   --version, -v             print the version
```

### Second

When you know how to play(work) with 'jf', you can enjoy it!
* curl command with `jf` [use pipline]
```bash
curl "http://api.examle.com/info" | jf 
```
some other commands can use the pipline with `jf`, such as 'echo'
```bash
echo '{"name": "ityike", "email": "yuanfeng634@gmail.com"}' | jf 
# result
{
    "name": "ityike",
    "email": "yuanfeng634@gmail.com"
}
```

* `jf` json data from file

```bash
jf -i ./test.txt
# result
{
    "name": "ityike",
    "email": "yuanfeng634@gmail.com"
}
```

* `jf` json data put into file

```bash 
echo '{"name": "ityike", "email": "yuanfeng634@gmail.com"}' | jf -o ./test.json
```

OR 
```bash
jf -o ./test.json
{"name": "ityike", "email": "yuanfeng634@gmail.com"}
# EOF by CTRL+D(Unix/Linux) or CTRL+Z(Win)
```

## Thanks!

Thanks [cli](https://github.com/urfave/cli) -- a package for building command line apps in Go