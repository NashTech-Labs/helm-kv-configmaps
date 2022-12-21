# Helm - ConfigMaps 

This template will show you how you can create configmaps of Key-value pairs direct from **env or conf files** & also from **Values.yaml**


## Prerequisites

1. Helm v3 installed
2. Basic knowledge of go-templates

### NOTE: key-values in files should like these

**Correct**

```s
name=application
version=1.0
type=backend
URL=https://example.com?x=y&z=w
```

**Incorrect**

```s
name=application label=cart   //Incorrect - multiple k-v in single line
version="1.0"                 //Incorrect - double-quoted not allowed
type = backend                //Incorrect - should not separated by spaces
```



## Usage

### 1. Just place files in `configkeyvalue/tmp/` directory 

**Optionally**

Place file contents in `values.yaml` file

### 2. Check Helm template

```
helm template demo configkeyvalue
```
