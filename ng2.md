Angular 2
=========

## Brad Green @bradlygreen, Google

Angular 1 October, 2015 about 1.1M devs. March 2016 about 1.3M. Angular 2 316K in March 2016.

> Angular 2 is in the final days

### Strategy

* Desktop Site
* Mobile Site
* Mobile App
* Desktop App

Have an "apps team" that can build apps across all these environments. Angular 2 can help.

Modern web stack with headroom for the future. Lazy loading.

Rendering layer can include components, module, pre-render.

Have a CLI. Intellisense component which gives IDEs more knowledge about your ng2 app and debug.

ngUpgrade to help with the transition.

Also has a goal to be very small and very fast. 2x faster than ng1 on initial render.
4.2x faster on re-render. But now, they're doing code generation now they're ~5x.

Production apps use code generation, you lose the dynamic engine, but its prod ready.
As if you did it in vanilla JS (doubts).

Service workers. Cache, Sync, Offline support.

Initial load: Angular Universal, Angular runs on the server. Generates HTML, CSS and starts sending JS.
Works in Node.js. Working on .NET, PHP/Twig, Java.

Web Workers demo.

roblog.io/js-repaint-perfs

Support Installed Mobile. ng1 was tied to the DOM. ng2 has different renders, including ionic,
NativeScript and React Native.

Electron and ng1. ng2 + electron is faster b/c its not on the UI thread. Access to platform APIs.

Windows Universal. Similar to electron, but gives access to Win32 and .NET APIs.

The idea is that all this enables all apps teams to speak the same langauge/framework.
