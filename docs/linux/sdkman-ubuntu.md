# How I use SDKMAN on Ubuntu

## Install SDKMAN

> [!WARNING]
> **Never execute sdk with sudo!**

Instructions to follow on ubuntu.

```bash
sudo apt update
sudo apt install -y curl zip unzip
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
```

## Install a JDK

To install a JDK, for example, from Azul, do:

List all the java available and filter it using a keyword like **zulu**

```bash
sdk list java | grep -i zulu
```

Pick one version and install it

```bash
sdk install java 21.0.19-zulu
```

Set it as default

```bash
sdk default java 21.0.19-zulu

```

Check it:

```bash
which java
java -version
echo "$JAVA_HOME"
```

## Switch to another JDK for a single terminal

To switch of JDK for a **single terminal** first list all the installed JDKs:

```bash
sdk list java | grep installed
```

If the required JDK is not listed, install it with the previous procedure but **do not set it by default** unless you want it.

Now set the required jdk to the terminal using:

```bash
set use java 21.0.5-zulu
```
