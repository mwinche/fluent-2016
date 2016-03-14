This talk is not available offline
==================================

 ## Alex Rickabaugh @synalx, Google

Mosh (mobile shell replacement for SSH), designed to work on a non-ideal network.

Mosh didn't improve the network, but it improved his experience. It did this by
being instantly available, it doesn't assume an ideal environment.

Our app should be designed for reality like Mosh.

3 step offline plane:

1. App is openable offline
2. Cache the initial data load
3. Make the app installable (manifest file)

Load static content *without* the network. This is called the 'app shell'. The already
does this. New deployment model: changing when content is downloaded.

Two APIs:

### Application Cache

Seems straightforward but easy to misuse

Declare all static content up front in a manifest.

Browser sees the manifest and downloads everything.

Your app works offline!

Manifest needs to be versioned.

Need to add network section, more gotchas to come.

Normal HTTP caching rules still apply, to the URLs in your manifest or even the manifest itself!

### Service Worker

Better but not supported everywhere yet.

Run a "server" on the client. Outgoing requests for the the worker first. Respond... or not.

See slides, I got behind here. He has code examples.

CacheStorageAPI, has request matching built in.

sw-precache which can generate service workers.

Can cache API calls if it makes sense (Avatars for instance). We can do this using sw-toolbox.
Network first will provide a fallback if the network fails. But might take along time
before the request is abandoned. But you can control how long you're willing to wait.

### Initial data load

Change the approach from a Promise to an Observable. First, we'll get from the cache
then from the network. Add `readFromCache` and `readFromNetwork` to your services.

### Make it installable

Signal that its installable with manifest. We will get an app like experience,
control screen orientation, remove chrome, icon on homescreen, plus other benefits.

It can be really hard to tell that its not native.

http://github.com/angular/answers-app/tree/fluent
