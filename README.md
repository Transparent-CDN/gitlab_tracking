# gitlab_tracking (Redmine 2.5.1+)

Gitlab messages parsing webhook

<center>
<img src="https://raw.githubusercontent.com/alfss/gitlab_tracking/master/example.png" alt="example">
</center>


## Installation
```
cd /my/redmine/root/path/plugins
git clone https://github.com/Transparent-CDN/gitlab_tracking
RAILS_ENV=production bundle exec rake redmine:plugins:migrate # For production, remove for development.
```


## Usage

regexp search in commit message:
```
    ((fix|ref)\s*#?[0-9]+)
```
<center>
<img src="https://raw.githubusercontent.com/alfss/gitlab_tracking/master/example2.png" alt="example">
</center>


webhook url:
```
    http://redmine[:port]/gitlab_tracking/webhook_parsing
```
 
settings plugin in redmine:
```
    https://redmine.site.ru/settings/plugin/gitlab_tracking
```

## Notes
- Plugin has been modified from the original one to hide the tracking for users that can't see private notes. The correct way would be generating a new permission and assigning it (TBD).
- It would be nice to validate the request with gitlab configured token.
