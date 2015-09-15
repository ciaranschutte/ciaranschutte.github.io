While looking up more angular resources, I was reminded of Firebase and realised it would be perfect for this project. So I removed the express components and created a <a href="https://github.com/ciaranschutte/scavenger">new repo.</a>

Originally I had looked into CouchDB as a simple way to get started but Firebase has too many awesome features to resist. This app is intended as an active event, having organizers constantly pieces of data that participants need to see immediately. Syncing this across clients is easy with Firebase. We could use GeoFire library but we're not actually querying a lot of new coordinates, just keeping track of a handful.

Additionally there's a great library for Angular, <a href="https://github.com/firebase/angularfire">AngularFire</a> as well as great support for Ionic. Offline sync looks easy to set up too, which could be very useful for this app!

Not using Express made me search for the easiest way to serve the site now. Originally I was going to fire up a Python SimpleHTTPServer but seen as I'm now a Gulp convert I found a <a href="https://github.com/nkt/gulp-serve">Gulp plugin</a> of course! 

Important lesson learnt; spend more time architecting* the fullstack before writing code. Even though I only had a very light Express erver with a couple of routes, it's still time wasted.

*<a href="http://c2.com/cgi/wiki?ArchitectingWord">interesting aside</a>

Also I came across a great method to hide important pieces of data like passwords and access keys, which can be found <a href="http://mindthecode.com/how-to-use-environment-variables-in-your-angular-application/">here</a>, although I skipped to the bottom for the module bit. I looked into Node libraries similar to PHPs dotenv library but creating an Angular module to use as a config block works great. There's an example <a href="https://github.com/ciaranschutte/scavenger/blob/master/public/example.config.js">here in the repo.</a>
