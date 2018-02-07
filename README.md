# eclipse-ide-java
Unofficial .deb Packages of the Eclipse IDE for Java EE Developers for Ubuntu

## Adding the ppa to Ubuntu

``sudo apt-add-repository ppa:threew82/eclipse-ide-jee``

``sudo apt-get update``

``sudo apt-get install eclipse-ide-jee``

## Contributing

### Install Debian developer tools

```
$ sudo apt-get install devscripts build-essential lintian
```

## Rename package directory

```
mv eclipse-ide-java-* <new eclipse version>
cd <new eclipse version>
```

All the magic happens in this directory.

## Rename orig package

```
mv eclipse-ide-jee_*orig.tar.gz eclipse-ide-jee_<new version>.orig.tar.gz
```

### Modify changelog

Modify `debian/changelog` file, inserting your name and modification **on top**
of the file.

## Modify preinst

Modify `debian/preinst` with the correct URL to download Eclipse for.

## Build your package

`$ debuild -us -uc`

## Test your package

`$ sudo dpkg -i ../eclipse-ide-jee_<new eclipse version>-1_amd64.deb`

## Push your changes

Open a branch, send us your modifications and wait for merging.
