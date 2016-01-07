# loki-localforage-adapter
A localforage adapter for lokijs

# usage

var lfAdapter = new LokiLocalForageAdapter("lokidb");
var db = new loki('databaseName',
                              { // optional options
                                // autoload: true,
                                // autoloadCallback : lokidb_loadHandler,
                                // autosave: true,
                                // autosaveInterval: 10000,
                                adapter: lfAdapter // <- required
                              });
db.loadDatabase({}, function() {
    console.log('done loading lokidb');
    lokidb_loadHandler(); // <- load any collections in here
});