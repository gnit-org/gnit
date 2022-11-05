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
