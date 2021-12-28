# imdb_dump
Created using arangodump
$arangodump --server.endpoint tcp://localhost:8529 --server.username root --server.database imdb3 --include-system-collections true -output-directory imdb3_dump

Use arangorestore to restore
$ arangorestore -c none --server.endpoint "tcp://127.0.0.1:8529"  --server.username "root" --server.database imdb3 --create-database true --force-same-database --include-system-collections  --input-directory imdb3_dump/
