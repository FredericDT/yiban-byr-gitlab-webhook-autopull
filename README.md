# gitlab-webhook-autopull

A php tiny http server for auto pull with a git remote

# Usage

1. clone this repo.

2. go to the repo's settings page and set "URL", "Secret Token"

3. copy the server's public_key to git_remote's integration_key field

4. edit 'gitlab.webhook.autopull.php' as follows
```
$exec_pair = [
    "secret-token" 
    =>
    "cd /path/to/the/project && git pull"
];
```

5. exec the following command as daemon

```
php -S listen.to.address:port gitlab.webhook.autopull.php
```
