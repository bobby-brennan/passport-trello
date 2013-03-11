Trello strategy for [passport](http://passportjs.org/)
- - -

Simple usage (CoffeeScript):

```coffeescript
passport.use 'trello', new TrelloStrategy(
    consumerKey: TRELLO_ID
    consumerSecret: TRELLO_SECRET
    callbackURL: TRELLO_CALLBACK
    passReqToCallback: true
    trelloParams:
        scope: "read,write"
        name: "MyApp"
        expiration: "never"
    (req, token, tokenSecret, profile, done) ->
        if not req.user
            # user is not authenticated, log in via trello or do something else
        else
            # authorize user to use Trello api
)
```