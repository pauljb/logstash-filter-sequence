This filter will assign events with the same timestamp a sequence so they can be displayed in correct order, by sorting on the sequence.


Get going:

1) Clone to /opt (as example)
```	
git clone https://github.com/pauljb/logstash-filter-sequence.git
```
2) Build
```
    cd /opt/logstash-filter-sequence
    gem build logstash-filter-sequence.gemspec
```
3) Install
```
    bin/plugin install /opt/logstash-filter-sequence/logstash-filter-sequence-0.1.1.gem
```

  The code for this plugin is originally from here:  https://logstash.jira.com/browse/LOGSTASH-192


Use in Logstash:

Use after any multiline filter you may have as such:
```
    sequence{}
```


Sort on sequence from elastic search.

e.g. /_search?sort=@timestamp,sequence
