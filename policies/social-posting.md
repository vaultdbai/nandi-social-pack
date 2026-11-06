---
name: Social posting stays with a person
applies_to: [agent:social-manager]
browser:
  refuse:
    - controls: [post, publish, share, send, tweet, reply, repost, schedule]
      kinds: [submit]
      sites: [linkedin.com, x.com, twitter.com, facebook.com, instagram.com, youtube.com]
      except: [start a post]
      say: Hand it over with browser_hand_over; the person presses it.
    - controls: [like, react, follow, connect, message, subscribe, invite]
      say: Never automated. Leave it to the person.
---

Social Manager prepares posts; a person publishes them.

The platforms' rules (LinkedIn's user agreement, X's automation rules, Meta's and Google's terms) ban scripts that operate their websites. So on the social sites this policy refuses the controls that publish (Post, Publish, Share, Send, Tweet, Reply, Repost, Schedule) and any submit: Enter, Ctrl+Enter, a submit button. The agent hands the page over instead, and the person presses Post.

Everywhere, it refuses likes, reactions, follows, connection requests, invitations, messages and subscriptions. These get accounts suspended and are never automated.

"Start a post" only opens LinkedIn's composer, so it isn't refused.
