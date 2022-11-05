# gnit

G-nit's
N-ot
T-witter 


Just a thought exercise covering some of the challenges in creating a fan out networks like Twitter.

Elements that need detailing:
- User segmentation
- Front end/web stack
- Microservices to support mobile
- iOS stack
- Android stack
- Backend store
- User segmentations
- Read path
  - Active users
  - Passive users
- Write path
- APIs/ecosystem

Goals for thought exercise:
- 10M readers daily, 90% of reads during 12 daylight hours of their time zone
- 1M posters daily, 5 posts per
- 100k media posts daily (2% of tweets)
- 10% of all users "active" - need updates <5s
- 50% of all users "passive-ish" - should see tweets ~1M old after logging in
- Permanant public cold storage (eg IPFS)
- Heavy use of caching - including distributed history

------

Michael's thoughts to include:

Divy up read and write path (Send Tweet user journey)

Write path: 
 - Publish Events (from tweet to store) --> Used by read path
 - Generate graph (you + top followers) for immediate vs delayed broadcast
 - Eventually consistent

Read path:
 - Subscribe to event
 - Populate self feed
 - Hydrate top followers immediately < X secs
 - Gradually rollout tweet to passive followers

Definitions required
1. Top followers (active all the time, need more or less instant notification - depends on client i.e firehose)
2. Slow followers (not active, tweet shows up when they login next i.e passive intent based feed view)

Not even getting into how we manage metadata management (such as geolocation to i8n to a11y)

Note: this doesn't get yet into media mgmt (a whole separate problem)
