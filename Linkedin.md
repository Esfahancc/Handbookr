# Auto connect
[My Network](https://www.linkedin.com/mynetwork/)
```
var i = 0;var connector = setInterval(() => {i++;if (i % 5 == 0) {window.scrollTo(0, document.body.scrollHeight);} else {window.scrollTo(0, 0);}if (i % 20 == 0) {if ($('.ip-fuse-limit-alert').length > 0){clearInterval(connector);}$('button[data-control-name="invite"],.mn-suggested-card__action-btn').each(function () {$(this).click();$(this).closest('li.mn-discovery-entity-card--with-coverphoto').remove();console.log('connected');});}}, 500);
```

# Auto unfollow
[Following](https://www.linkedin.com/feed/following/?filterType=connection)
```
var i = 0;var unfollower = setInterval(() => {i++;if (i % 5 == 0) {window.scrollTo(0, document.body.scrollHeight);} else {window.scrollTo(0, 0);}if (i % 200 == 0) {$('[data-control-name="actor_follow_toggle"][aria-pressed="true"]').each(function(){$(this).click();$(this).closest('li.follows-recommendation-card').remove();console.log('unfollowed');});}}, 500);
```
