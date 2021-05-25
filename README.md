# Elasticsearch Bash API

This is a command-line library for interacting with ElasticSearch built on BASH.

## Usage

Each command has configurations that determine how the commands are viewed etc. These are controlled through environment variables. Arguments necessary for the commands are positional arguments.

For example, if you want an overview of a specific index you can run:

```bash
$ ./elastic/indices-overview-by-name <indexName>
```

If you want to view it with column headings, set 'v'.

```bash
$ v=true ./elastic/indices-overview-by-name <indexName>
```

For help use `-h` as the firt argument.

```bash
$ ./elastic/custer-health -h
```

## Configuration

The 'bootstrap' script determines the library path. If you want to change the library path then do so with:

```bash
$ export ELASTICSEARCH_BASH_API_PATH=/the/path
```

Set up the HTTP URL to ElasticSearch. Defaults to: http://0.0.0.0:9200

```bash
$ export ELASTICSEARCH_HOST="http://0.0.0.0:9200"
```

This will have to be run every time you open a terminal, or be put into your `.bashrc`.

## Reference

The following material was used to put this together:

- https://gist.github.com/ruanbekker/e8a09604b14f37e8d2f743a87b930f93#indices-overview