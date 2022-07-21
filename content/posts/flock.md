---
title: How to prevent a cron job from running multiple times
date: 2013-04-06
emoji: 👨‍⚕️
---

Sometimes a cron job might run slower, then you anticipated. Many instances of it stack up.

You could increase the time interval during starts of the cron job - but this could lead to further problems down the road.

Fortunately there is an easy and clean fix.

Just replace your cronjob with this:

```bash
/usr/bin/flock -n /var/lock/<foobar> <long-running-task>
```

Whenever your cron job is started a lock file will be created and no other instance can start.

## Conclusion

This a simple remedy for colliding cron job's. I use it frequently.