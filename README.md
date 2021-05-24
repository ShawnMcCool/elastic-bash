# Elasticsearch Bash API

This is a command-line library for interacting with ElasticSearch built on BASH.

## Usage

Each command has configurations that determine how the commands are viewed etc. These are controlled through environment variables. Arguments necessary for the commands are positional arguments.

For example, if you want an overview of a specific index you can run:

```shell
$ ./elastic/indices-overview-by-name <indexName>
```

If you want to view it with column headings, set 'v'.

```shell
$ v=true ./elastic/indices-overview-by-name <indexName>
```

For help use `-h` as the firt argument.

```shell
$ ./elastic/custer-health -h
```

## Configuration

The 'bootstrap' script determines the library path. If you want to change the library path then do so with:

```shell
$ export ELASTICSEARCH_BASH_API_PATH=/the/path
```

This will have to be run every time you open a terminal, or be put into your `.bashrc`.