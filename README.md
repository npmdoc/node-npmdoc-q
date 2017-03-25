# api documentation for  [q (v1.5.0)](https://github.com/kriskowal/q)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-q.svg)](https://travis-ci.org/npmdoc/node-npmdoc-q)
#### A library for promises (CommonJS/Promises/A,B,D)

[![NPM](https://nodei.co/npm/q.png?downloads=true)](https://www.npmjs.com/package/q)

[![apidoc](https://npmdoc.github.io/node-npmdoc-q/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-q_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-q/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-q/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Kris Kowal",
        "email": "kris@cixar.com",
        "url": "https://github.com/kriskowal"
    },
    "bugs": {
        "url": "http://github.com/kriskowal/q/issues"
    },
    "contributors": [
        {
            "name": "Kris Kowal",
            "email": "kris@cixar.com",
            "url": "https://github.com/kriskowal"
        },
        {
            "name": "Irakli Gozalishvili",
            "email": "rfobic@gmail.com",
            "url": "http://jeditoolkit.com"
        },
        {
            "name": "Domenic Denicola",
            "email": "domenic@domenicdenicola.com",
            "url": "http://domenicdenicola.com"
        }
    ],
    "dependencies": {},
    "description": "A library for promises (CommonJS/Promises/A,B,D)",
    "devDependencies": {
        "cover": "*",
        "grunt": "~0.4.1",
        "grunt-cli": "~0.1.9",
        "grunt-contrib-uglify": "~0.9.1",
        "jasmine-node": "1.11.0",
        "jshint": "~2.1.9",
        "matcha": "~0.2.0",
        "opener": "*",
        "promises-aplus-tests": "1.x"
    },
    "directories": {
        "test": "./spec"
    },
    "dist": {
        "shasum": "dd01bac9d06d30e6f219aecb8253ee9ebdc308f1",
        "tarball": "https://registry.npmjs.org/q/-/q-1.5.0.tgz"
    },
    "engines": {
        "node": ">=0.6.0",
        "teleport": ">=0.2.0"
    },
    "files": [
        "LICENSE",
        "q.js",
        "queue.js"
    ],
    "gitHead": "4fecabe07ff9f3683a3d4548e7f81c2aba693326",
    "homepage": "https://github.com/kriskowal/q",
    "keywords": [
        "q",
        "promise",
        "promises",
        "promises-a",
        "promises-aplus",
        "deferred",
        "future",
        "async",
        "flow control",
        "fluent",
        "browser",
        "node"
    ],
    "license": "MIT",
    "main": "q.js",
    "maintainers": [
        {
            "name": "kriskowal",
            "email": "kris.kowal@cixar.com"
        },
        {
            "name": "domenic",
            "email": "domenic@domenicdenicola.com"
        }
    ],
    "name": "q",
    "optionalDependencies": {},
    "overlay": {
        "teleport": {
            "dependencies": {
                "system": ">=0.0.4"
            }
        }
    },
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/kriskowal/q.git"
    },
    "scripts": {
        "benchmark": "matcha",
        "cover": "cover run jasmine-node spec && cover report html && opener cover_html/index.html",
        "lint": "jshint q.js",
        "minify": "grunt",
        "prepublish": "grunt",
        "test": "npm ls -s && jasmine-node spec && promises-aplus-tests spec/aplus-adapter && npm run -s lint",
        "test-browser": "opener spec/q-spec.html"
    },
    "version": "1.5.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module q](#apidoc.module.q)
1.  boolean <span class="apidocSignatureSpan">q.</span>longStackSupport
1.  [function <span class="apidocSignatureSpan">q.</span>Promise (resolver)](#apidoc.element.q.Promise)
1.  [function <span class="apidocSignatureSpan">q.</span>all (promises)](#apidoc.element.q.all)
1.  [function <span class="apidocSignatureSpan">q.</span>allResolved ()](#apidoc.element.q.allResolved)
1.  [function <span class="apidocSignatureSpan">q.</span>allSettled (promises)](#apidoc.element.q.allSettled)
1.  [function <span class="apidocSignatureSpan">q.</span>any (promises)](#apidoc.element.q.any)
1.  [function <span class="apidocSignatureSpan">q.</span>async (makeGenerator)](#apidoc.element.q.async)
1.  [function <span class="apidocSignatureSpan">q.</span>catch (object, rejected)](#apidoc.element.q.catch)
1.  [function <span class="apidocSignatureSpan">q.</span>defer ()](#apidoc.element.q.defer)
1.  [function <span class="apidocSignatureSpan">q.</span>del (object, key)](#apidoc.element.q.del)
1.  [function <span class="apidocSignatureSpan">q.</span>delay (object, timeout)](#apidoc.element.q.delay)
1.  [function <span class="apidocSignatureSpan">q.</span>delete (object, key)](#apidoc.element.q.delete)
1.  [function <span class="apidocSignatureSpan">q.</span>denodeify (callback)](#apidoc.element.q.denodeify)
1.  [function <span class="apidocSignatureSpan">q.</span>dispatch (object, op, args)](#apidoc.element.q.dispatch)
1.  [function <span class="apidocSignatureSpan">q.</span>done (object, fulfilled, rejected, progress)](#apidoc.element.q.done)
1.  [function <span class="apidocSignatureSpan">q.</span>fail (object, rejected)](#apidoc.element.q.fail)
1.  [function <span class="apidocSignatureSpan">q.</span>fapply (object, args)](#apidoc.element.q.fapply)
1.  [function <span class="apidocSignatureSpan">q.</span>fbind (object)](#apidoc.element.q.fbind)
1.  [function <span class="apidocSignatureSpan">q.</span>fcall (object)](#apidoc.element.q.fcall)
1.  [function <span class="apidocSignatureSpan">q.</span>fin (object, callback)](#apidoc.element.q.fin)
1.  [function <span class="apidocSignatureSpan">q.</span>finally (object, callback)](#apidoc.element.q.finally)
1.  [function <span class="apidocSignatureSpan">q.</span>fulfill (value)](#apidoc.element.q.fulfill)
1.  [function <span class="apidocSignatureSpan">q.</span>get (object, key)](#apidoc.element.q.get)
1.  [function <span class="apidocSignatureSpan">q.</span>getUnhandledReasons ()](#apidoc.element.q.getUnhandledReasons)
1.  [function <span class="apidocSignatureSpan">q.</span>invoke (object, name)](#apidoc.element.q.invoke)
1.  [function <span class="apidocSignatureSpan">q.</span>isFulfilled (object)](#apidoc.element.q.isFulfilled)
1.  [function <span class="apidocSignatureSpan">q.</span>isPending (object)](#apidoc.element.q.isPending)
1.  [function <span class="apidocSignatureSpan">q.</span>isPromise (object)](#apidoc.element.q.isPromise)
1.  [function <span class="apidocSignatureSpan">q.</span>isPromiseAlike (object)](#apidoc.element.q.isPromiseAlike)
1.  [function <span class="apidocSignatureSpan">q.</span>isRejected (object)](#apidoc.element.q.isRejected)
1.  [function <span class="apidocSignatureSpan">q.</span>join (x, y)](#apidoc.element.q.join)
1.  [function <span class="apidocSignatureSpan">q.</span>keys (object)](#apidoc.element.q.keys)
1.  [function <span class="apidocSignatureSpan">q.</span>makePromise (descriptor, fallback, inspect)](#apidoc.element.q.makePromise)
1.  [function <span class="apidocSignatureSpan">q.</span>mapply (object, name, args)](#apidoc.element.q.mapply)
1.  [function <span class="apidocSignatureSpan">q.</span>master (object)](#apidoc.element.q.master)
1.  [function <span class="apidocSignatureSpan">q.</span>mcall (object, name)](#apidoc.element.q.mcall)
1.  [function <span class="apidocSignatureSpan">q.</span>nbind (callback, thisp)](#apidoc.element.q.nbind)
1.  [function <span class="apidocSignatureSpan">q.</span>nearer (value)](#apidoc.element.q.nearer)
1.  [function <span class="apidocSignatureSpan">q.</span>nextTick (task)](#apidoc.element.q.nextTick)
1.  [function <span class="apidocSignatureSpan">q.</span>nfapply (callback, args)](#apidoc.element.q.nfapply)
1.  [function <span class="apidocSignatureSpan">q.</span>nfbind (callback)](#apidoc.element.q.nfbind)
1.  [function <span class="apidocSignatureSpan">q.</span>nfcall (callback)](#apidoc.element.q.nfcall)
1.  [function <span class="apidocSignatureSpan">q.</span>ninvoke (object, name)](#apidoc.element.q.ninvoke)
1.  [function <span class="apidocSignatureSpan">q.</span>nmapply (object, name, args)](#apidoc.element.q.nmapply)
1.  [function <span class="apidocSignatureSpan">q.</span>nmcall (object, name)](#apidoc.element.q.nmcall)
1.  [function <span class="apidocSignatureSpan">q.</span>noConflict ()](#apidoc.element.q.noConflict)
1.  [function <span class="apidocSignatureSpan">q.</span>nodeify (object, nodeback)](#apidoc.element.q.nodeify)
1.  [function <span class="apidocSignatureSpan">q.</span>npost (object, name, args)](#apidoc.element.q.npost)
1.  [function <span class="apidocSignatureSpan">q.</span>nsend (object, name)](#apidoc.element.q.nsend)
1.  [function <span class="apidocSignatureSpan">q.</span>passByCopy (object)](#apidoc.element.q.passByCopy)
1.  [function <span class="apidocSignatureSpan">q.</span>post (object, name, args)](#apidoc.element.q.post)
1.  [function <span class="apidocSignatureSpan">q.</span>progress (object, progressed)](#apidoc.element.q.progress)
1.  [function <span class="apidocSignatureSpan">q.</span>promise (resolver)](#apidoc.element.q.promise)
1.  [function <span class="apidocSignatureSpan">q.</span>promised (callback)](#apidoc.element.q.promised)
1.  [function <span class="apidocSignatureSpan">q.</span>race (answerPs)](#apidoc.element.q.race)
1.  [function <span class="apidocSignatureSpan">q.</span>reject (reason)](#apidoc.element.q.reject)
1.  [function <span class="apidocSignatureSpan">q.</span>resetUnhandledRejections ()](#apidoc.element.q.resetUnhandledRejections)
1.  [function <span class="apidocSignatureSpan">q.</span>resolve (value)](#apidoc.element.q.resolve)
1.  [function <span class="apidocSignatureSpan">q.</span>return (value)](#apidoc.element.q.return)
1.  [function <span class="apidocSignatureSpan">q.</span>send (object, name)](#apidoc.element.q.send)
1.  [function <span class="apidocSignatureSpan">q.</span>set (object, key, value)](#apidoc.element.q.set)
1.  [function <span class="apidocSignatureSpan">q.</span>spawn (makeGenerator)](#apidoc.element.q.spawn)
1.  [function <span class="apidocSignatureSpan">q.</span>spread (value, fulfilled, rejected)](#apidoc.element.q.spread)
1.  [function <span class="apidocSignatureSpan">q.</span>stopUnhandledRejectionTracking ()](#apidoc.element.q.stopUnhandledRejectionTracking)
1.  [function <span class="apidocSignatureSpan">q.</span>tap (promise, callback)](#apidoc.element.q.tap)
1.  [function <span class="apidocSignatureSpan">q.</span>thenReject (promise, reason)](#apidoc.element.q.thenReject)
1.  [function <span class="apidocSignatureSpan">q.</span>thenResolve (promise, value)](#apidoc.element.q.thenResolve)
1.  [function <span class="apidocSignatureSpan">q.</span>timeout (object, ms, error)](#apidoc.element.q.timeout)
1.  [function <span class="apidocSignatureSpan">q.</span>try (object)](#apidoc.element.q.try)
1.  [function <span class="apidocSignatureSpan">q.</span>when (value, fulfilled, rejected, progressed)](#apidoc.element.q.when)
1.  object <span class="apidocSignatureSpan">q.</span>defer.prototype
1.  object <span class="apidocSignatureSpan">q.</span>makePromise.prototype

#### [module q.Promise](#apidoc.module.q.Promise)
1.  [function <span class="apidocSignatureSpan">q.</span>Promise (resolver)](#apidoc.element.q.Promise.Promise)
1.  [function <span class="apidocSignatureSpan">q.Promise.</span>all (promises)](#apidoc.element.q.Promise.all)
1.  [function <span class="apidocSignatureSpan">q.Promise.</span>race (answerPs)](#apidoc.element.q.Promise.race)
1.  [function <span class="apidocSignatureSpan">q.Promise.</span>reject (reason)](#apidoc.element.q.Promise.reject)
1.  [function <span class="apidocSignatureSpan">q.Promise.</span>resolve (value)](#apidoc.element.q.Promise.resolve)

#### [module q.defer](#apidoc.module.q.defer)
1.  [function <span class="apidocSignatureSpan">q.</span>defer ()](#apidoc.element.q.defer.defer)

#### [module q.defer.prototype](#apidoc.module.q.defer.prototype)
1.  [function <span class="apidocSignatureSpan">q.defer.prototype.</span>makeNodeResolver ()](#apidoc.element.q.defer.prototype.makeNodeResolver)

#### [module q.makePromise](#apidoc.module.q.makePromise)
1.  [function <span class="apidocSignatureSpan">q.</span>makePromise (descriptor, fallback, inspect)](#apidoc.element.q.makePromise.makePromise)

#### [module q.makePromise.prototype](#apidoc.module.q.makePromise.prototype)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>all ()](#apidoc.element.q.makePromise.prototype.all)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>allResolved ()](#apidoc.element.q.makePromise.prototype.allResolved)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>allSettled ()](#apidoc.element.q.makePromise.prototype.allSettled)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>any ()](#apidoc.element.q.makePromise.prototype.any)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>catch (rejected)](#apidoc.element.q.makePromise.prototype.catch)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>del (key)](#apidoc.element.q.makePromise.prototype.del)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>delay (timeout)](#apidoc.element.q.makePromise.prototype.delay)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>delete (key)](#apidoc.element.q.makePromise.prototype.delete)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>denodeify ()](#apidoc.element.q.makePromise.prototype.denodeify)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>dispatch (op, args)](#apidoc.element.q.makePromise.prototype.dispatch)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>done (fulfilled, rejected, progress)](#apidoc.element.q.makePromise.prototype.done)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fail (rejected)](#apidoc.element.q.makePromise.prototype.fail)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fapply (args)](#apidoc.element.q.makePromise.prototype.fapply)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fbind ()](#apidoc.element.q.makePromise.prototype.fbind)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fcall ()](#apidoc.element.q.makePromise.prototype.fcall)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fin (callback)](#apidoc.element.q.makePromise.prototype.fin)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>finally (callback)](#apidoc.element.q.makePromise.prototype.finally)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>get (key)](#apidoc.element.q.makePromise.prototype.get)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>invoke (name)](#apidoc.element.q.makePromise.prototype.invoke)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>isFulfilled ()](#apidoc.element.q.makePromise.prototype.isFulfilled)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>isPending ()](#apidoc.element.q.makePromise.prototype.isPending)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>isRejected ()](#apidoc.element.q.makePromise.prototype.isRejected)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>join (that)](#apidoc.element.q.makePromise.prototype.join)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>keys ()](#apidoc.element.q.makePromise.prototype.keys)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>mapply (name, args)](#apidoc.element.q.makePromise.prototype.mapply)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>mcall (name)](#apidoc.element.q.makePromise.prototype.mcall)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nbind ()](#apidoc.element.q.makePromise.prototype.nbind)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nfapply (args)](#apidoc.element.q.makePromise.prototype.nfapply)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nfbind ()](#apidoc.element.q.makePromise.prototype.nfbind)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nfcall ()](#apidoc.element.q.makePromise.prototype.nfcall)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>ninvoke (name)](#apidoc.element.q.makePromise.prototype.ninvoke)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nmapply (name, args)](#apidoc.element.q.makePromise.prototype.nmapply)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nmcall (name)](#apidoc.element.q.makePromise.prototype.nmcall)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nodeify (nodeback)](#apidoc.element.q.makePromise.prototype.nodeify)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>npost (name, args)](#apidoc.element.q.makePromise.prototype.npost)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nsend (name)](#apidoc.element.q.makePromise.prototype.nsend)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>passByCopy ()](#apidoc.element.q.makePromise.prototype.passByCopy)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>post (name, args)](#apidoc.element.q.makePromise.prototype.post)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>progress (progressed)](#apidoc.element.q.makePromise.prototype.progress)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>race ()](#apidoc.element.q.makePromise.prototype.race)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>send (name)](#apidoc.element.q.makePromise.prototype.send)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>set (key, value)](#apidoc.element.q.makePromise.prototype.set)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>spread (fulfilled, rejected)](#apidoc.element.q.makePromise.prototype.spread)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>tap (callback)](#apidoc.element.q.makePromise.prototype.tap)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>then (fulfilled, rejected, progressed)](#apidoc.element.q.makePromise.prototype.then)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>thenReject (reason)](#apidoc.element.q.makePromise.prototype.thenReject)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>thenResolve (value)](#apidoc.element.q.makePromise.prototype.thenResolve)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>timeout (ms, error)](#apidoc.element.q.makePromise.prototype.timeout)
1.  [function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>toString ()](#apidoc.element.q.makePromise.prototype.toString)

#### [module q.nextTick](#apidoc.module.q.nextTick)
1.  [function <span class="apidocSignatureSpan">q.</span>nextTick (task)](#apidoc.element.q.nextTick.nextTick)
1.  [function <span class="apidocSignatureSpan">q.nextTick.</span>runAfter (task)](#apidoc.element.q.nextTick.runAfter)



# <a name="apidoc.module.q"></a>[module q](#apidoc.module.q)

#### <a name="apidoc.element.q.Promise"></a>[function <span class="apidocSignatureSpan">q.</span>Promise (resolver)](#apidoc.element.q.Promise)
- description and source-code
```javascript
function promise(resolver) {
    if (typeof resolver !== "function") {
        throw new TypeError("resolver must be a function.");
    }
    var deferred = defer();
    try {
        resolver(deferred.resolve, deferred.reject, deferred.notify);
    } catch (reason) {
        deferred.reject(reason);
    }
    return deferred.promise;
}
```
- example usage
```shell
...
This is an alternative promise-creation API that has the same power as
the deferred concept, but without introducing another conceptual entity.

Rewriting the 'requestOkText' example above using 'Q.Promise':

'''javascript
function requestOkText(url) {
    return Q.Promise(function(resolve, reject, notify) {
var request = new XMLHttpRequest();

request.open("GET", url, true);
request.onload = onload;
request.onerror = onerror;
request.onprogress = onprogress;
request.send();
...
```

#### <a name="apidoc.element.q.all"></a>[function <span class="apidocSignatureSpan">q.</span>all (promises)](#apidoc.element.q.all)
- description and source-code
```javascript
function all(promises) {
    return when(promises, function (promises) {
        var pendingCount = 0;
        var deferred = defer();
        array_reduce(promises, function (undefined, promise, index) {
            var snapshot;
            if (
                isPromise(promise) &&
                (snapshot = promise.inspect()).state === "fulfilled"
            ) {
                promises[index] = snapshot.value;
            } else {
                ++pendingCount;
                when(
                    promise,
                    function (value) {
                        promises[index] = value;
                        if (--pendingCount === 0) {
                            deferred.resolve(promises);
                        }
                    },
                    deferred.reject,
                    function (progress) {
                        deferred.notify({ index: index, value: progress });
                    }
                );
            }
        }, void 0);
        if (pendingCount === 0) {
            deferred.resolve(promises);
        }
        return deferred.promise;
    });
}
```
- example usage
```shell
...

### Combination

You can turn an array of promises into a promise for the whole,
fulfilled array using ''all''.

'''javascript
return Q.all([
    eventualAdd(2, 2),
    eventualAdd(10, 20)
]);
'''

If you have a promise for an array, you can use ''spread'' as a
replacement for ''then''.  The ''spread'' function “spreads” the
...
```

#### <a name="apidoc.element.q.allResolved"></a>[function <span class="apidocSignatureSpan">q.</span>allResolved ()](#apidoc.element.q.allResolved)
- description and source-code
```javascript
allResolved = function () {
    if (typeof console !== "undefined" &&
        typeof console.warn === "function") {
        console.warn(name + " is deprecated, use " + alternative +
                     " instead.", new Error("").stack);
    }
    return callback.apply(callback, arguments);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.allSettled"></a>[function <span class="apidocSignatureSpan">q.</span>allSettled (promises)](#apidoc.element.q.allSettled)
- description and source-code
```javascript
function allSettled(promises) {
    return Q(promises).allSettled();
}
```
- example usage
```shell
...
promise is fulfilled, the array contains the fulfillment values of the original
promises, in the same order as those promises.  If one of the given promises
is rejected, the returned promise is immediately rejected, not waiting for the
rest of the batch.  If you want to wait for all of the promises to either be
fulfilled or rejected, you can use ''allSettled''.

'''javascript
Q.allSettled(promises)
.then(function (results) {
results.forEach(function (result) {
    if (result.state === "fulfilled") {
        var value = result.value;
    } else {
        var reason = result.reason;
    }
...
```

#### <a name="apidoc.element.q.any"></a>[function <span class="apidocSignatureSpan">q.</span>any (promises)](#apidoc.element.q.any)
- description and source-code
```javascript
function any(promises) {
    if (promises.length === 0) {
        return Q.resolve();
    }

    var deferred = Q.defer();
    var pendingCount = 0;
    array_reduce(promises, function (prev, current, index) {
        var promise = promises[index];

        pendingCount++;

        when(promise, onFulfilled, onRejected, onProgress);
        function onFulfilled(result) {
            deferred.resolve(result);
        }
        function onRejected(err) {
            pendingCount--;
            if (pendingCount === 0) {
                err.message = ("Q can't get fulfillment value from any promise, all " +
                    "promises were rejected. Last error message: " + err.message);
                deferred.reject(err);
            }
        }
        function onProgress(progress) {
            deferred.notify({
                index: index,
                value: progress
            });
        }
    }, undefined);

    return deferred.promise;
}
```
- example usage
```shell
...
'''

The ''any'' function accepts an array of promises and returns a promise that is
fulfilled by the first given promise to be fulfilled, or rejected if all of the
given promises are rejected.

'''javascript
Q.any(promises)
.then(function (first) {
    // Any of the promises was fulfilled.
}, function (error) {
    // All of the promises were rejected.
});
'''
...
```

#### <a name="apidoc.element.q.async"></a>[function <span class="apidocSignatureSpan">q.</span>async (makeGenerator)](#apidoc.element.q.async)
- description and source-code
```javascript
function async(makeGenerator) {
    return function () {
        // when verb is "send", arg is a value
        // when verb is "throw", arg is an exception
        function continuer(verb, arg) {
            var result;

            // Until V8 3.19 / Chromium 29 is released, SpiderMonkey is the only
            // engine that has a deployed base of browsers that support generators.
            // However, SM's generators use the Python-inspired semantics of
            // outdated ES6 drafts.  We would like to support ES6, but we'd also
            // like to make it possible to use generators in deployed browsers, so
            // we also support Python-style generators.  At some point we can remove
            // this block.

            if (typeof StopIteration === "undefined") {
                // ES6 Generators
                try {
                    result = generator[verb](arg);
                } catch (exception) {
                    return reject(exception);
                }
                if (result.done) {
                    return Q(result.value);
                } else {
                    return when(result.value, callback, errback);
                }
            } else {
                // SpiderMonkey Generators
                // FIXME: Remove this case when SM does ES6 generators.
                try {
                    result = generator[verb](arg);
                } catch (exception) {
                    if (isStopIteration(exception)) {
                        return Q(exception.value);
                    } else {
                        return reject(exception);
                    }
                }
                return when(result, callback, errback);
            }
        }
        var generator = makeGenerator.apply(this, arguments);
        var callback = continuer.bind(continuer, "next");
        var errback = continuer.bind(continuer, "throw");
        return callback();
    };
}
```
- example usage
```shell
...
* calls the generator and also ends the promise chain, so that any
* unhandled errors are thrown instead of forwarded to the error
* handler. This is useful because it's extremely common to run
* generators at the top-level to work with libraries.
*/
Q.spawn = spawn;
function spawn(makeGenerator) {
   Q.done(Q.async(makeGenerator)());
}

// FIXME: Remove this interface once ES6 generators are in SpiderMonkey.
/**
* Throws a ReturnValue exception to stop an asynchronous generator.
*
* This interface is a stop-gap measure to support generator return
...
```

#### <a name="apidoc.element.q.catch"></a>[function <span class="apidocSignatureSpan">q.</span>catch (object, rejected)](#apidoc.element.q.catch)
- description and source-code
```javascript
catch = function (object, rejected) {
    return Q(object).then(void 0, rejected);
}
```
- example usage
```shell
...
Q.fcall(promisedStep1)
.then(promisedStep2)
.then(promisedStep3)
.then(promisedStep4)
.then(function (value4) {
    // Do something with value4
})
.catch(function (error) {
    // Handle any error from all above steps
})
.done();
'''

With this approach, you also get implicit error propagation, just like 'try',
'catch', and 'finally'.  An error in 'promisedStep1' will flow all the way to
...
```

#### <a name="apidoc.element.q.defer"></a>[function <span class="apidocSignatureSpan">q.</span>defer ()](#apidoc.element.q.defer)
- description and source-code
```javascript
function defer() {
    // if "messages" is an "Array", that indicates that the promise has not yet
    // been resolved.  If it is "undefined", it has been resolved.  Each
    // element of the messages array is itself an array of complete arguments to
    // forward to the resolved promise.  We coerce the resolution value to a
    // promise using the 'resolve' function because it handles both fully
    // non-thenable values and other thenables gracefully.
    var messages = [], progressListeners = [], resolvedPromise;

    var deferred = object_create(defer.prototype);
    var promise = object_create(Promise.prototype);

    promise.promiseDispatch = function (resolve, op, operands) {
        var args = array_slice(arguments);
        if (messages) {
            messages.push(args);
            if (op === "when" && operands[1]) { // progress operand
                progressListeners.push(operands[1]);
            }
        } else {
            Q.nextTick(function () {
                resolvedPromise.promiseDispatch.apply(resolvedPromise, args);
            });
        }
    };

    // XXX deprecated
    promise.valueOf = function () {
        if (messages) {
            return promise;
        }
        var nearerValue = nearer(resolvedPromise);
        if (isPromise(nearerValue)) {
            resolvedPromise = nearerValue; // shorten chain
        }
        return nearerValue;
    };

    promise.inspect = function () {
        if (!resolvedPromise) {
            return { state: "pending" };
        }
        return resolvedPromise.inspect();
    };

    if (Q.longStackSupport && hasStacks) {
        try {
            throw new Error();
        } catch (e) {
            // NOTE: don't try to use 'Error.captureStackTrace' or transfer the
            // accessor around; that causes memory leaks as per GH-111. Just
            // reify the stack trace as a string ASAP.
            //
            // At the same time, cut off the first line; it's always just
            // "[object Promise]\n", as per the 'toString'.
            promise.stack = e.stack.substring(e.stack.indexOf("\n") + 1);
            promise.stackCounter = longStackCounter++;
        }
    }

    // NOTE: we do the checks for 'resolvedPromise' in each method, instead of
    // consolidating them into 'become', since otherwise we'd create new
    // promises with the lines 'become(whatever(value))'. See e.g. GH-252.

    function become(newPromise) {
        resolvedPromise = newPromise;

        if (Q.longStackSupport && hasStacks) {
            // Only hold a reference to the new promise if long stacks
            // are enabled to reduce memory usage
            promise.source = newPromise;
        }

        array_reduce(messages, function (undefined, message) {
            Q.nextTick(function () {
                newPromise.promiseDispatch.apply(newPromise, message);
            });
        }, void 0);

        messages = void 0;
        progressListeners = void 0;
    }

    deferred.promise = promise;
    deferred.resolve = function (value) {
        if (resolvedPromise) {
            return;
        }

        become(Q(value));
    };

    deferred.fulfill = function (value) {
        if (resolvedPromise) {
            return;
        }

        become(fulfill(value));
    };
    deferred.reject = function (reason) {
        if (resolvedPromise) {
            return;
        }

        become(reject(reason));
    };
    deferred.notify = function (progress) {
        if (resolvedPromise) {
            return;
        }

        array_reduce(progressListeners, function (undefined, progressListener) {
            Q.nextTick(function () {
                progressListener(progress);
            });
        }, void 0);
    };

    return deferred;
}
```
- example usage
```shell
...
#### Using Deferreds

If you have to interface with asynchronous functions that are callback-based
instead of promise-based, Q provides a few shortcuts (like ''Q.nfcall'' and
friends). But much of the time, the solution will be to use *deferreds*.

'''javascript
var deferred = Q.defer();
FS.readFile("foo.txt", "utf-8", function (error, text) {
    if (error) {
        deferred.reject(new Error(error));
    } else {
        deferred.resolve(text);
    }
});
...
```

#### <a name="apidoc.element.q.del"></a>[function <span class="apidocSignatureSpan">q.</span>del (object, key)](#apidoc.element.q.del)
- description and source-code
```javascript
del = function (object, key) {
    return Q(object).dispatch("delete", [key]);
}
```
- example usage
```shell
...
promises, so they can be chained.

'''
direct manipulation         using a promise as a proxy
--------------------------  -------------------------------
value.foo                   promise.get("foo")
value.foo = value           promise.put("foo", value)
delete value.foo            promise.del("foo")
value.foo(...args)          promise.post("foo", [args])
value.foo(...args)          promise.invoke("foo", ...args)
value(...args)              promise.fapply([args])
value(...args)              promise.fcall(...args)
'''

If the promise is a proxy for a remote object, you can shave
...
```

#### <a name="apidoc.element.q.delay"></a>[function <span class="apidocSignatureSpan">q.</span>delay (object, timeout)](#apidoc.element.q.delay)
- description and source-code
```javascript
delay = function (object, timeout) {
    if (timeout === void 0) {
        timeout = object;
        object = void 0;
    }
    return Q(object).delay(timeout);
}
```
- example usage
```shell
...

Q comes with optional support for “long stack traces,” wherein the 'stack'
property of 'Error' rejection reasons is rewritten to be traced along
asynchronous jumps instead of stopping at the most recent one. As an example:

'''js
function theDepthsOfMyProgram() {
  Q.delay(100).done(function explode() {
    throw new Error("boo!");
  });
}

theDepthsOfMyProgram();
'''
...
```

#### <a name="apidoc.element.q.delete"></a>[function <span class="apidocSignatureSpan">q.</span>delete (object, key)](#apidoc.element.q.delete)
- description and source-code
```javascript
delete = function (object, key) {
    return Q(object).dispatch("delete", [key]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.denodeify"></a>[function <span class="apidocSignatureSpan">q.</span>denodeify (callback)](#apidoc.element.q.denodeify)
- description and source-code
```javascript
denodeify = function (callback) {
    if (callback === undefined) {
        throw new Error("Q can't wrap an undefined function");
    }
    var baseArgs = array_slice(arguments, 1);
    return function () {
        var nodeArgs = baseArgs.concat(array_slice(arguments));
        var deferred = defer();
        nodeArgs.push(deferred.makeNodeResolver());
        Q(callback).fapply(nodeArgs).fail(deferred.reject);
        return deferred.promise;
    };
}
```
- example usage
```shell
...
return Q.ninvoke(redisClient, "get", "user:1:id");
return Q.npost(redisClient, "get", ["user:1:id"]);
'''

You can also create reusable wrappers with 'Q.denodeify' or 'Q.nbind':

'''javascript
var readFile = Q.denodeify(FS.readFile);
return readFile("foo.txt", "utf-8");

var redisClientGet = Q.nbind(redisClient.get, redisClient);
return redisClientGet("user:1:id");
'''

Finally, if you're working with raw deferred objects, there is a
...
```

#### <a name="apidoc.element.q.dispatch"></a>[function <span class="apidocSignatureSpan">q.</span>dispatch (object, op, args)](#apidoc.element.q.dispatch)
- description and source-code
```javascript
function dispatch(object, op, args) {
    return Q(object).dispatch(op, args);
}
```
- example usage
```shell
...
 * @param object* the recipient
 * @param op the name of the message operation, e.g., "when",
 * @param args further arguments to be forwarded to the operation
 * @returns result {Promise} a promise for the result of the operation
 */
Q.dispatch = dispatch;
function dispatch(object, op, args) {
return Q(object).dispatch(op, args);
}

Promise.prototype.dispatch = function (op, args) {
var self = this;
var deferred = defer();
Q.nextTick(function () {
    self.promiseDispatch(deferred.resolve, op, args);
...
```

#### <a name="apidoc.element.q.done"></a>[function <span class="apidocSignatureSpan">q.</span>done (object, fulfilled, rejected, progress)](#apidoc.element.q.done)
- description and source-code
```javascript
done = function (object, fulfilled, rejected, progress) {
    return Q(object).done(fulfilled, rejected, progress);
}
```
- example usage
```shell
...
.then(promisedStep4)
.then(function (value4) {
    // Do something with value4
})
.catch(function (error) {
    // Handle any error from all above steps
})
.done();
'''

With this approach, you also get implicit error propagation, just like 'try',
'catch', and 'finally'.  An error in 'promisedStep1' will flow all the way to
the 'catch' function, where it’s caught and handled.  (Here 'promisedStepN' is
a version of 'stepN' that returns a promise.)
...
```

#### <a name="apidoc.element.q.fail"></a>[function <span class="apidocSignatureSpan">q.</span>fail (object, rejected)](#apidoc.element.q.fail)
- description and source-code
```javascript
fail = function (object, rejected) {
    return Q(object).then(void 0, rejected);
}
```
- example usage
```shell
...
'''

Q promises provide a ''fail'' shorthand for ''then'' when you are only
interested in handling the error:

'''javascript
var outputPromise = getInputPromise()
.fail(function (error) {
});
'''

If you are writing JavaScript for modern engines only or using
CoffeeScript, you may use 'catch' instead of 'fail'.

Promises also have a ''fin'' function that is like a ''finally'' clause.
...
```

#### <a name="apidoc.element.q.fapply"></a>[function <span class="apidocSignatureSpan">q.</span>fapply (object, args)](#apidoc.element.q.fapply)
- description and source-code
```javascript
fapply = function (object, args) {
    return Q(object).dispatch("apply", [void 0, args]);
}
```
- example usage
```shell
...
direct manipulation         using a promise as a proxy
--------------------------  -------------------------------
value.foo                   promise.get("foo")
value.foo = value           promise.put("foo", value)
delete value.foo            promise.del("foo")
value.foo(...args)          promise.post("foo", [args])
value.foo(...args)          promise.invoke("foo", ...args)
value(...args)              promise.fapply([args])
value(...args)              promise.fcall(...args)
'''

If the promise is a proxy for a remote object, you can shave
round-trips by using these functions instead of ''then''.  To take
advantage of promises for remote objects, check out [Q-Connection][].
...
```

#### <a name="apidoc.element.q.fbind"></a>[function <span class="apidocSignatureSpan">q.</span>fbind (object)](#apidoc.element.q.fbind)
- description and source-code
```javascript
fbind = function (object) {
    var promise = Q(object);
    var args = array_slice(arguments, 1);
    return function fbound() {
        return promise.dispatch("apply", [
            this,
            args.concat(array_slice(arguments))
        ]);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.fcall"></a>[function <span class="apidocSignatureSpan">q.</span>fcall (object)](#apidoc.element.q.fcall)
- description and source-code
```javascript
fcall = function (object) {
    return Q(object).dispatch("apply", [void 0, array_slice(arguments, 1)]);
}
```
- example usage
```shell
...
    });
});
'''

With a promise library, you can flatten the pyramid.

'''javascript
Q.fcall(promisedStep1)
.then(promisedStep2)
.then(promisedStep3)
.then(promisedStep4)
.then(function (value4) {
    // Do something with value4
})
.catch(function (error) {
...
```

#### <a name="apidoc.element.q.fin"></a>[function <span class="apidocSignatureSpan">q.</span>fin (object, callback)](#apidoc.element.q.fin)
- description and source-code
```javascript
fin = function (object, callback) {
    return Q(object)["finally"](callback);
}
```
- example usage
```shell
...
returned by ''getInputPromise()'' either returns a value or throws an
error.  The value returned or error thrown by ''getInputPromise()''
passes directly to ''outputPromise'' unless the final handler fails, and
may be delayed if the final handler returns a promise.

'''javascript
var outputPromise = getInputPromise()
.fin(function () {
    // close files, database connections, stop servers, conclude tests
});
'''

-   If the handler returns a value, the value is ignored
-   If the handler throws an error, the error passes to ''outputPromise''
-   If the handler returns a promise, ''outputPromise'' gets postponed.  The
...
```

#### <a name="apidoc.element.q.finally"></a>[function <span class="apidocSignatureSpan">q.</span>finally (object, callback)](#apidoc.element.q.finally)
- description and source-code
```javascript
finally = function (object, callback) {
    return Q(object)["finally"](callback);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.fulfill"></a>[function <span class="apidocSignatureSpan">q.</span>fulfill (value)](#apidoc.element.q.fulfill)
- description and source-code
```javascript
function fulfill(value) {
    return Promise({
        "when": function () {
            return value;
        },
        "get": function (name) {
            return value[name];
        },
        "set": function (name, rhs) {
            value[name] = rhs;
        },
        "delete": function (name) {
            delete value[name];
        },
        "post": function (name, args) {
            // Mark Miller proposes that post with no name should apply a
            // promised function.
            if (name === null || name === void 0) {
                return value.apply(void 0, args);
            } else {
                return value[name].apply(value, args);
            }
        },
        "apply": function (thisp, args) {
            return value.apply(thisp, args);
        },
        "keys": function () {
            return object_keys(value);
        }
    }, void 0, function inspect() {
        return { state: "fulfilled", value: value };
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.get"></a>[function <span class="apidocSignatureSpan">q.</span>get (object, key)](#apidoc.element.q.get)
- description and source-code
```javascript
get = function (object, key) {
    return Q(object).dispatch("get", [key]);
}
```
- example usage
```shell
...
object.  There are methods that allow you to optimistically manipulate
properties or call functions.  All of these interactions return
promises, so they can be chained.

'''
direct manipulation         using a promise as a proxy
--------------------------  -------------------------------
value.foo                   promise.get("foo")
value.foo = value           promise.put("foo", value)
delete value.foo            promise.del("foo")
value.foo(...args)          promise.post("foo", [args])
value.foo(...args)          promise.invoke("foo", ...args)
value(...args)              promise.fapply([args])
value(...args)              promise.fcall(...args)
'''
...
```

#### <a name="apidoc.element.q.getUnhandledReasons"></a>[function <span class="apidocSignatureSpan">q.</span>getUnhandledReasons ()](#apidoc.element.q.getUnhandledReasons)
- description and source-code
```javascript
getUnhandledReasons = function () {
    // Make a copy so that consumers can't interfere with our internal state.
    return unhandledReasons.slice();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.invoke"></a>[function <span class="apidocSignatureSpan">q.</span>invoke (object, name)](#apidoc.element.q.invoke)
- description and source-code
```javascript
invoke = function (object, name) {
    return Q(object).dispatch("post", [name, array_slice(arguments, 2)]);
}
```
- example usage
```shell
...
'''

If there is any chance that the promise you receive is not a Q promise
as provided by your library, you should wrap it using a Q function.
You can even use ''Q.invoke'' as a shorthand.

'''javascript
return Q.invoke($, 'ajax', ...)
.then(function () {
});
'''


### Over the Wire
...
```

#### <a name="apidoc.element.q.isFulfilled"></a>[function <span class="apidocSignatureSpan">q.</span>isFulfilled (object)](#apidoc.element.q.isFulfilled)
- description and source-code
```javascript
function isFulfilled(object) {
    return !isPromise(object) || object.inspect().state === "fulfilled";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.isPending"></a>[function <span class="apidocSignatureSpan">q.</span>isPending (object)](#apidoc.element.q.isPending)
- description and source-code
```javascript
function isPending(object) {
    return isPromise(object) && object.inspect().state === "pending";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.isPromise"></a>[function <span class="apidocSignatureSpan">q.</span>isPromise (object)](#apidoc.element.q.isPromise)
- description and source-code
```javascript
function isPromise(object) {
    return object instanceof Promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.isPromiseAlike"></a>[function <span class="apidocSignatureSpan">q.</span>isPromiseAlike (object)](#apidoc.element.q.isPromiseAlike)
- description and source-code
```javascript
function isPromiseAlike(object) {
    return isObject(object) && typeof object.then === "function";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.isRejected"></a>[function <span class="apidocSignatureSpan">q.</span>isRejected (object)](#apidoc.element.q.isRejected)
- description and source-code
```javascript
function isRejected(object) {
    return isPromise(object) && object.inspect().state === "rejected";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.join"></a>[function <span class="apidocSignatureSpan">q.</span>join (x, y)](#apidoc.element.q.join)
- description and source-code
```javascript
join = function (x, y) {
    return Q(x).join(y);
}
```
- example usage
```shell
...
        if (p.stack && (!error.__minimumStackCounter__ || error.__minimumStackCounter__ > p.stackCounter)) {
            object_defineProperty(error, "__minimumStackCounter__", {value: p.stackCounter, configurable: true});
            stacks.unshift(p.stack);
        }
    }
    stacks.unshift(error.stack);

    var concatedStacks = stacks.join("\n" + STACK_JUMP_SEPARATOR + "\n");
    var stack = filterStackString(concatedStacks);
    object_defineProperty(error, "stack", {value: stack, configurable: true});
}
}

function filterStackString(stackString) {
var lines = stackString.split("\n");
...
```

#### <a name="apidoc.element.q.keys"></a>[function <span class="apidocSignatureSpan">q.</span>keys (object)](#apidoc.element.q.keys)
- description and source-code
```javascript
keys = function (object) {
    return Q(object).dispatch("keys", []);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise"></a>[function <span class="apidocSignatureSpan">q.</span>makePromise (descriptor, fallback, inspect)](#apidoc.element.q.makePromise)
- description and source-code
```javascript
function Promise(descriptor, fallback, inspect) {
    if (fallback === void 0) {
        fallback = function (op) {
            return reject(new Error(
                "Promise does not support operation: " + op
            ));
        };
    }
    if (inspect === void 0) {
        inspect = function () {
            return {state: "unknown"};
        };
    }

    var promise = object_create(Promise.prototype);

    promise.promiseDispatch = function (resolve, op, args) {
        var result;
        try {
            if (descriptor[op]) {
                result = descriptor[op].apply(promise, args);
            } else {
                result = fallback.call(promise, op, args);
            }
        } catch (exception) {
            result = reject(exception);
        }
        if (resolve) {
            resolve(result);
        }
    };

    promise.inspect = inspect;

    // XXX deprecated 'valueOf' and 'exception' support
    if (inspect) {
        var inspected = inspect();
        if (inspected.state === "rejected") {
            promise.exception = inspected.reason;
        }

        promise.valueOf = function () {
            var inspected = inspect();
            if (inspected.state === "pending" ||
                inspected.state === "rejected") {
                return promise;
            }
            return inspected.value;
        };
    }

    return promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.mapply"></a>[function <span class="apidocSignatureSpan">q.</span>mapply (object, name, args)](#apidoc.element.q.mapply)
- description and source-code
```javascript
mapply = function (object, name, args) {
    return Q(object).dispatch("post", [name, args]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.master"></a>[function <span class="apidocSignatureSpan">q.</span>master (object)](#apidoc.element.q.master)
- description and source-code
```javascript
function master(object) {
    return Promise({
        "isDef": function () {}
    }, function fallback(op, args) {
        return dispatch(object, op, args);
    }, function () {
        return Q(object).inspect();
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.mcall"></a>[function <span class="apidocSignatureSpan">q.</span>mcall (object, name)](#apidoc.element.q.mcall)
- description and source-code
```javascript
mcall = function (object, name) {
    return Q(object).dispatch("post", [name, array_slice(arguments, 2)]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.nbind"></a>[function <span class="apidocSignatureSpan">q.</span>nbind (callback, thisp)](#apidoc.element.q.nbind)
- description and source-code
```javascript
nbind = function (callback, thisp) {
    var baseArgs = array_slice(arguments, 2);
    return function () {
        var nodeArgs = baseArgs.concat(array_slice(arguments));
        var deferred = defer();
        nodeArgs.push(deferred.makeNodeResolver());
        function bound() {
            return callback.apply(thisp, arguments);
        }
        Q(bound).fapply(nodeArgs).fail(deferred.reject);
        return deferred.promise;
    };
}
```
- example usage
```shell
...

You can also create reusable wrappers with 'Q.denodeify' or 'Q.nbind':

'''javascript
var readFile = Q.denodeify(FS.readFile);
return readFile("foo.txt", "utf-8");

var redisClientGet = Q.nbind(redisClient.get, redisClient);
return redisClientGet("user:1:id");
'''

Finally, if you're working with raw deferred objects, there is a
'makeNodeResolver' method on deferreds that can be handy:

'''javascript
...
```

#### <a name="apidoc.element.q.nearer"></a>[function <span class="apidocSignatureSpan">q.</span>nearer (value)](#apidoc.element.q.nearer)
- description and source-code
```javascript
function nearer(value) {
    if (isPromise(value)) {
        var inspected = value.inspect();
        if (inspected.state === "fulfilled") {
            return inspected.value;
        }
    }
    return value;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.nextTick"></a>[function <span class="apidocSignatureSpan">q.</span>nextTick (task)](#apidoc.element.q.nextTick)
- description and source-code
```javascript
nextTick = function (task) {
    tail = tail.next = {
        task: task,
        domain: isNodeJS && process.domain,
        next: null
    };

    if (!flushing) {
        flushing = true;
        requestTick();
    }
}
```
- example usage
```shell
...
    //   'setTimeout'. In this case 'setImmediate' is preferred because
    //    it is faster. Browserify's 'process.toString()' yields
    //   "[object Object]", while in a real Node environment
    //   'process.toString()' yields "[object process]".
    isNodeJS = true;

    requestTick = function () {
        process.nextTick(flush);
    };

} else if (typeof setImmediate === "function") {
    // In IE10, Node.js 0.9+, or https://github.com/NobleJS/setImmediate
    if (typeof window !== "undefined") {
        requestTick = setImmediate.bind(window, flush);
    } else {
...
```

#### <a name="apidoc.element.q.nfapply"></a>[function <span class="apidocSignatureSpan">q.</span>nfapply (callback, args)](#apidoc.element.q.nfapply)
- description and source-code
```javascript
nfapply = function (callback, args) {
    return Q(callback).nfapply(args);
}
```
- example usage
```shell
...
where callbacks are in the form of 'function(err, result)', Q provides a few
useful utility functions for converting between them. The most straightforward
are probably 'Q.nfcall' and 'Q.nfapply' ("Node function call/apply") for calling
Node.js-style functions and getting back a promise:

'''javascript
return Q.nfcall(FS.readFile, "foo.txt", "utf-8");
return Q.nfapply(FS.readFile, ["foo.txt", "utf-8"]);
'''

If you are working with methods, instead of simple functions, you can easily
run in to the usual problems where passing a method to another function—like
'Q.nfcall'—"un-binds" the method from its owner. To avoid this, you can either
use 'Function.prototype.bind' or some nice shortcut methods we provide:
...
```

#### <a name="apidoc.element.q.nfbind"></a>[function <span class="apidocSignatureSpan">q.</span>nfbind (callback)](#apidoc.element.q.nfbind)
- description and source-code
```javascript
nfbind = function (callback) {
    if (callback === undefined) {
        throw new Error("Q can't wrap an undefined function");
    }
    var baseArgs = array_slice(arguments, 1);
    return function () {
        var nodeArgs = baseArgs.concat(array_slice(arguments));
        var deferred = defer();
        nodeArgs.push(deferred.makeNodeResolver());
        Q(callback).fapply(nodeArgs).fail(deferred.reject);
        return deferred.promise;
    };
}
```
- example usage
```shell
...
return deferred.promise;
};

/**
 * Wraps a NodeJS continuation passing function and returns an equivalent
 * version that returns a promise.
 * @example
 * Q.nfbind(FS.readFile, __filename)("utf-8")
 * .then(console.log)
 * .done()
 */
Q.nfbind =
Q.denodeify = function (callback /*...args*/) {
if (callback === undefined) {
    throw new Error("Q can't wrap an undefined function");
...
```

#### <a name="apidoc.element.q.nfcall"></a>[function <span class="apidocSignatureSpan">q.</span>nfcall (callback)](#apidoc.element.q.nfcall)
- description and source-code
```javascript
nfcall = function (callback) {
    var args = array_slice(arguments, 1);
    return Q(callback).nfapply(args);
}
```
- example usage
```shell
...
If you're working with functions that make use of the Node.js callback pattern,
where callbacks are in the form of 'function(err, result)', Q provides a few
useful utility functions for converting between them. The most straightforward
are probably 'Q.nfcall' and 'Q.nfapply' ("Node function call/apply") for calling
Node.js-style functions and getting back a promise:

'''javascript
return Q.nfcall(FS.readFile, "foo.txt", "utf-8");
return Q.nfapply(FS.readFile, ["foo.txt", "utf-8"]);
'''

If you are working with methods, instead of simple functions, you can easily
run in to the usual problems where passing a method to another function—like
'Q.nfcall'—"un-binds" the method from its owner. To avoid this, you can either
use 'Function.prototype.bind' or some nice shortcut methods we provide:
...
```

#### <a name="apidoc.element.q.ninvoke"></a>[function <span class="apidocSignatureSpan">q.</span>ninvoke (object, name)](#apidoc.element.q.ninvoke)
- description and source-code
```javascript
ninvoke = function (object, name) {
    var nodeArgs = array_slice(arguments, 2);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    Q(object).dispatch("post", [name, nodeArgs]).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
...

If you are working with methods, instead of simple functions, you can easily
run in to the usual problems where passing a method to another function—like
'Q.nfcall'—"un-binds" the method from its owner. To avoid this, you can either
use 'Function.prototype.bind' or some nice shortcut methods we provide:

'''javascript
return Q.ninvoke(redisClient, "get", "user:1:id");
return Q.npost(redisClient, "get", ["user:1:id"]);
'''

You can also create reusable wrappers with 'Q.denodeify' or 'Q.nbind':

'''javascript
var readFile = Q.denodeify(FS.readFile);
...
```

#### <a name="apidoc.element.q.nmapply"></a>[function <span class="apidocSignatureSpan">q.</span>nmapply (object, name, args)](#apidoc.element.q.nmapply)
- description and source-code
```javascript
nmapply = function (object, name, args) {
    return Q(object).npost(name, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.nmcall"></a>[function <span class="apidocSignatureSpan">q.</span>nmcall (object, name)](#apidoc.element.q.nmcall)
- description and source-code
```javascript
nmcall = function (object, name) {
    var nodeArgs = array_slice(arguments, 2);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    Q(object).dispatch("post", [name, nodeArgs]).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.noConflict"></a>[function <span class="apidocSignatureSpan">q.</span>noConflict ()](#apidoc.element.q.noConflict)
- description and source-code
```javascript
noConflict = function () {
    throw new Error("Q.noConflict only works when Q is used as a global");
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.nodeify"></a>[function <span class="apidocSignatureSpan">q.</span>nodeify (object, nodeback)](#apidoc.element.q.nodeify)
- description and source-code
```javascript
function nodeify(object, nodeback) {
    return Q(object).nodeify(nodeback);
}
```
- example usage
```shell
...
 * pass a nodeback, they will receive the result promise.
 * @param object a result (or a promise for a result)
 * @param {Function} nodeback a Node.js-style callback
 * @returns either the promise or nothing
 */
Q.nodeify = nodeify;
function nodeify(object, nodeback) {
return Q(object).nodeify(nodeback);
}

Promise.prototype.nodeify = function (nodeback) {
if (nodeback) {
    this.then(function (value) {
        Q.nextTick(function () {
            nodeback(null, value);
...
```

#### <a name="apidoc.element.q.npost"></a>[function <span class="apidocSignatureSpan">q.</span>npost (object, name, args)](#apidoc.element.q.npost)
- description and source-code
```javascript
npost = function (object, name, args) {
    return Q(object).npost(name, args);
}
```
- example usage
```shell
...
If you are working with methods, instead of simple functions, you can easily
run in to the usual problems where passing a method to another function—like
'Q.nfcall'—"un-binds" the method from its owner. To avoid this, you can either
use 'Function.prototype.bind' or some nice shortcut methods we provide:

'''javascript
return Q.ninvoke(redisClient, "get", "user:1:id");
return Q.npost(redisClient, "get", ["user:1:id"]);
'''

You can also create reusable wrappers with 'Q.denodeify' or 'Q.nbind':

'''javascript
var readFile = Q.denodeify(FS.readFile);
return readFile("foo.txt", "utf-8");
...
```

#### <a name="apidoc.element.q.nsend"></a>[function <span class="apidocSignatureSpan">q.</span>nsend (object, name)](#apidoc.element.q.nsend)
- description and source-code
```javascript
nsend = function (object, name) {
    var nodeArgs = array_slice(arguments, 2);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    Q(object).dispatch("post", [name, nodeArgs]).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.passByCopy"></a>[function <span class="apidocSignatureSpan">q.</span>passByCopy (object)](#apidoc.element.q.passByCopy)
- description and source-code
```javascript
passByCopy = function (object) {
    //freeze(object);
    //passByCopies.set(object, true);
    return object;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.post"></a>[function <span class="apidocSignatureSpan">q.</span>post (object, name, args)](#apidoc.element.q.post)
- description and source-code
```javascript
post = function (object, name, args) {
    return Q(object).dispatch("post", [name, args]);
}
```
- example usage
```shell
...

'''
direct manipulation         using a promise as a proxy
--------------------------  -------------------------------
value.foo                   promise.get("foo")
value.foo = value           promise.put("foo", value)
delete value.foo            promise.del("foo")
value.foo(...args)          promise.post("foo", [args])
value.foo(...args)          promise.invoke("foo", ...args)
value(...args)              promise.fapply([args])
value(...args)              promise.fcall(...args)
'''

If the promise is a proxy for a remote object, you can shave
round-trips by using these functions instead of ''then''.  To take
...
```

#### <a name="apidoc.element.q.progress"></a>[function <span class="apidocSignatureSpan">q.</span>progress (object, progressed)](#apidoc.element.q.progress)
- description and source-code
```javascript
function progress(object, progressed) {
    return Q(object).then(void 0, void 0, progressed);
}
```
- example usage
```shell
...
});
'''

Like 'fail', Q also provides a shorthand for progress callbacks
called 'progress':

'''javascript
return uploadFile().progress(function (progress) {
    // We get notified of the upload's progress
});
'''

### The End

When you get to the end of a chain of promises, you should either
...
```

#### <a name="apidoc.element.q.promise"></a>[function <span class="apidocSignatureSpan">q.</span>promise (resolver)](#apidoc.element.q.promise)
- description and source-code
```javascript
function promise(resolver) {
    if (typeof resolver !== "function") {
        throw new TypeError("resolver must be a function.");
    }
    var deferred = defer();
    try {
        resolver(deferred.resolve, deferred.reject, deferred.notify);
    } catch (reason) {
        deferred.reject(reason);
    }
    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.promised"></a>[function <span class="apidocSignatureSpan">q.</span>promised (callback)](#apidoc.element.q.promised)
- description and source-code
```javascript
function promised(callback) {
    return function () {
        return spread([this, all(arguments)], function (self, args) {
            return callback.apply(self, args);
        });
    };
}
```
- example usage
```shell
...
/**
* The promised function decorator ensures that any promise arguments
* are settled and passed as values ('this' is also settled and passed
* as a value).  It will also ensure that the result of a function is
* always a promise.
*
* @example
* var add = Q.promised(function (a, b) {
*     return a + b;
* });
* add(Q(a), Q(B));
*
* @param {function} callback The function to decorate
* @returns {function} a function that has been decorated.
*/
...
```

#### <a name="apidoc.element.q.race"></a>[function <span class="apidocSignatureSpan">q.</span>race (answerPs)](#apidoc.element.q.race)
- description and source-code
```javascript
function race(answerPs) {
    return promise(function (resolve, reject) {
        // Switch to this once we can assume at least ES5
        // answerPs.forEach(function (answerP) {
        //     Q(answerP).then(resolve, reject);
        // });
        // Use this in the meantime
        for (var i = 0, len = answerPs.length; i < len; i++) {
            Q(answerPs[i]).then(resolve, reject);
        }
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.reject"></a>[function <span class="apidocSignatureSpan">q.</span>reject (reason)](#apidoc.element.q.reject)
- description and source-code
```javascript
function reject(reason) {
    var rejection = Promise({
        "when": function (rejected) {
            // note that the error has been handled
            if (rejected) {
                untrackRejection(this);
            }
            return rejected ? rejected(reason) : this;
        }
    }, function fallback() {
        return this;
    }, function inspect() {
        return { state: "rejected", reason: reason };
    });

    // Note that the reason has not been handled.
    trackRejection(rejection, reason);

    return rejection;
}
```
- example usage
```shell
...
instead of promise-based, Q provides a few shortcuts (like ''Q.nfcall'' and
friends). But much of the time, the solution will be to use *deferreds*.

'''javascript
var deferred = Q.defer();
FS.readFile("foo.txt", "utf-8", function (error, text) {
    if (error) {
        deferred.reject(new Error(error));
    } else {
        deferred.resolve(text);
    }
});
return deferred.promise;
'''
...
```

#### <a name="apidoc.element.q.resetUnhandledRejections"></a>[function <span class="apidocSignatureSpan">q.</span>resetUnhandledRejections ()](#apidoc.element.q.resetUnhandledRejections)
- description and source-code
```javascript
function resetUnhandledRejections() {
    unhandledReasons.length = 0;
    unhandledRejections.length = 0;

    if (!trackUnhandledRejections) {
        trackUnhandledRejections = true;
    }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.resolve"></a>[function <span class="apidocSignatureSpan">q.</span>resolve (value)](#apidoc.element.q.resolve)
- description and source-code
```javascript
function Q(value) {
    // If the object is already a Promise, return it directly.  This enables
    // the resolve function to both be used to created references from objects,
    // but to tolerably coerce non-promises to promises.
    if (value instanceof Promise) {
        return value;
    }

    // assimilate thenables
    if (isPromiseAlike(value)) {
        return coerce(value);
    } else {
        return fulfill(value);
    }
}
```
- example usage
```shell
...

'''javascript
var deferred = Q.defer();
FS.readFile("foo.txt", "utf-8", function (error, text) {
    if (error) {
        deferred.reject(new Error(error));
    } else {
        deferred.resolve(text);
    }
});
return deferred.promise;
'''

Note that a deferred can be resolved with a value or a promise.  The
''reject'' function is a shorthand for resolving with a rejected
...
```

#### <a name="apidoc.element.q.return"></a>[function <span class="apidocSignatureSpan">q.</span>return (value)](#apidoc.element.q.return)
- description and source-code
```javascript
function _return(value) {
    throw new QReturnValue(value);
}
```
- example usage
```shell
...
 *      var bar = yield getBarPromise();
 *      return foo + bar;
 * })
 * // Older SpiderMonkey style
 * Q.async(function () {
 *      var foo = yield getFooPromise();
 *      var bar = yield getBarPromise();
 *      Q.return(foo + bar);
 * })
 */
Q["return"] = _return;
function _return(value) {
    throw new QReturnValue(value);
}
...
```

#### <a name="apidoc.element.q.send"></a>[function <span class="apidocSignatureSpan">q.</span>send (object, name)](#apidoc.element.q.send)
- description and source-code
```javascript
send = function (object, name) {
    return Q(object).dispatch("post", [name, array_slice(arguments, 2)]);
}
```
- example usage
```shell
...
var request = new XMLHttpRequest();
var deferred = Q.defer();

request.open("GET", url, true);
request.onload = onload;
request.onerror = onerror;
request.onprogress = onprogress;
request.send();

function onload() {
    if (request.status === 200) {
        deferred.resolve(request.responseText);
    } else {
        deferred.reject(new Error("Status code was " + request.status));
    }
...
```

#### <a name="apidoc.element.q.set"></a>[function <span class="apidocSignatureSpan">q.</span>set (object, key, value)](#apidoc.element.q.set)
- description and source-code
```javascript
set = function (object, key, value) {
    return Q(object).dispatch("set", [key, value]);
}
```
- example usage
```shell
...
promise.resolve = Q; // ES6

// XXX experimental.  This method is a way to denote that a local value is
// serializable and should be immediately dispatched to a remote upon request,
// instead of passing a reference.
Q.passByCopy = function (object) {
//freeze(object);
//passByCopies.set(object, true);
return object;
};

Promise.prototype.passByCopy = function () {
//freeze(object);
//passByCopies.set(object, true);
return this;
...
```

#### <a name="apidoc.element.q.spawn"></a>[function <span class="apidocSignatureSpan">q.</span>spawn (makeGenerator)](#apidoc.element.q.spawn)
- description and source-code
```javascript
function spawn(makeGenerator) {
    Q.done(Q.async(makeGenerator)());
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.spread"></a>[function <span class="apidocSignatureSpan">q.</span>spread (value, fulfilled, rejected)](#apidoc.element.q.spread)
- description and source-code
```javascript
function spread(value, fulfilled, rejected) {
    return Q(value).spread(fulfilled, rejected);
}
```
- example usage
```shell
...
replacement for ''then''.  The ''spread'' function “spreads” the
values over the arguments of the fulfillment handler.  The rejection handler
will get called at the first sign of failure.  That is, whichever of
the received promises fails first gets handled by the rejection handler.

'''javascript
function eventualAdd(a, b) {
    return Q.spread([a, b], function (a, b) {
        return a + b;
    })
}
'''

But ''spread'' calls ''all'' initially, so you can skip it in chains.
...
```

#### <a name="apidoc.element.q.stopUnhandledRejectionTracking"></a>[function <span class="apidocSignatureSpan">q.</span>stopUnhandledRejectionTracking ()](#apidoc.element.q.stopUnhandledRejectionTracking)
- description and source-code
```javascript
stopUnhandledRejectionTracking = function () {
    resetUnhandledRejections();
    trackUnhandledRejections = false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.tap"></a>[function <span class="apidocSignatureSpan">q.</span>tap (promise, callback)](#apidoc.element.q.tap)
- description and source-code
```javascript
tap = function (promise, callback) {
    return Q(promise).tap(callback);
}
```
- example usage
```shell
...
       }
   }]);

   return deferred.promise;
};

Q.tap = function (promise, callback) {
   return Q(promise).tap(callback);
};

/**
* Works almost like "finally", but not called for rejections.
* Original resolution value is passed through callback unaffected.
* Callback may return a promise that will be awaited for.
* @param {Function} callback
...
```

#### <a name="apidoc.element.q.thenReject"></a>[function <span class="apidocSignatureSpan">q.</span>thenReject (promise, reason)](#apidoc.element.q.thenReject)
- description and source-code
```javascript
thenReject = function (promise, reason) {
    return Q(promise).thenReject(reason);
}
```
- example usage
```shell
...
};

Promise.prototype.thenReject = function (reason) {
   return this.then(function () { throw reason; });
};

Q.thenReject = function (promise, reason) {
   return Q(promise).thenReject(reason);
};

/**
* If an object is not a promise, it is as "near" as possible.
* If a promise is rejected, it is as "near" as possible too.
* If it’s a fulfilled promise, the fulfillment value is nearer.
* If it’s a deferred promise and the deferred has been resolved, the
...
```

#### <a name="apidoc.element.q.thenResolve"></a>[function <span class="apidocSignatureSpan">q.</span>thenResolve (promise, value)](#apidoc.element.q.thenResolve)
- description and source-code
```javascript
thenResolve = function (promise, value) {
    return Q(promise).thenResolve(value);
}
```
- example usage
```shell
...
*   .tap(console.log)
*   .then(...);
*/
Promise.prototype.tap = function (callback) {
   callback = Q(callback);

   return this.then(function (value) {
       return callback.fcall(value).thenResolve(value);
   });
};

/**
* Registers an observer on a promise.
*
* Guarantees:
...
```

#### <a name="apidoc.element.q.timeout"></a>[function <span class="apidocSignatureSpan">q.</span>timeout (object, ms, error)](#apidoc.element.q.timeout)
- description and source-code
```javascript
timeout = function (object, ms, error) {
    return Q(object).timeout(ms, error);
}
```
- example usage
```shell
...
 * @param {Any*} promise
 * @param {Number} milliseconds timeout
 * @param {Any*} custom error message or Error object (optional)
 * @returns a promise for the resolution of the given promise if it is
 * fulfilled before the timeout, otherwise rejected.
 */
Q.timeout = function (object, ms, error) {
return Q(object).timeout(ms, error);
};

Promise.prototype.timeout = function (ms, error) {
var deferred = defer();
var timeoutId = setTimeout(function () {
    if (!error || "string" === typeof error) {
        error = new Error(error || "Timed out after " + ms + " ms");
...
```

#### <a name="apidoc.element.q.try"></a>[function <span class="apidocSignatureSpan">q.</span>try (object)](#apidoc.element.q.try)
- description and source-code
```javascript
try = function (object) {
    return Q(object).dispatch("apply", [void 0, array_slice(arguments, 1)]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.when"></a>[function <span class="apidocSignatureSpan">q.</span>when (value, fulfilled, rejected, progressed)](#apidoc.element.q.when)
- description and source-code
```javascript
function when(value, fulfilled, rejected, progressed) {
    return Q(value).then(fulfilled, rejected, progressed);
}
```
- example usage
```shell
...
'''

This is a simplified implementation of ''Q.timeout''

'''javascript
function timeout(promise, ms) {
    var deferred = Q.defer();
    Q.when(promise, deferred.resolve);
    delay(ms).then(function () {
        deferred.reject(new Error("Timed out"));
    });
    return deferred.promise;
}
'''
...
```



# <a name="apidoc.module.q.Promise"></a>[module q.Promise](#apidoc.module.q.Promise)

#### <a name="apidoc.element.q.Promise.Promise"></a>[function <span class="apidocSignatureSpan">q.</span>Promise (resolver)](#apidoc.element.q.Promise.Promise)
- description and source-code
```javascript
function promise(resolver) {
    if (typeof resolver !== "function") {
        throw new TypeError("resolver must be a function.");
    }
    var deferred = defer();
    try {
        resolver(deferred.resolve, deferred.reject, deferred.notify);
    } catch (reason) {
        deferred.reject(reason);
    }
    return deferred.promise;
}
```
- example usage
```shell
...
This is an alternative promise-creation API that has the same power as
the deferred concept, but without introducing another conceptual entity.

Rewriting the 'requestOkText' example above using 'Q.Promise':

'''javascript
function requestOkText(url) {
    return Q.Promise(function(resolve, reject, notify) {
var request = new XMLHttpRequest();

request.open("GET", url, true);
request.onload = onload;
request.onerror = onerror;
request.onprogress = onprogress;
request.send();
...
```

#### <a name="apidoc.element.q.Promise.all"></a>[function <span class="apidocSignatureSpan">q.Promise.</span>all (promises)](#apidoc.element.q.Promise.all)
- description and source-code
```javascript
function all(promises) {
    return when(promises, function (promises) {
        var pendingCount = 0;
        var deferred = defer();
        array_reduce(promises, function (undefined, promise, index) {
            var snapshot;
            if (
                isPromise(promise) &&
                (snapshot = promise.inspect()).state === "fulfilled"
            ) {
                promises[index] = snapshot.value;
            } else {
                ++pendingCount;
                when(
                    promise,
                    function (value) {
                        promises[index] = value;
                        if (--pendingCount === 0) {
                            deferred.resolve(promises);
                        }
                    },
                    deferred.reject,
                    function (progress) {
                        deferred.notify({ index: index, value: progress });
                    }
                );
            }
        }, void 0);
        if (pendingCount === 0) {
            deferred.resolve(promises);
        }
        return deferred.promise;
    });
}
```
- example usage
```shell
...

### Combination

You can turn an array of promises into a promise for the whole,
fulfilled array using ''all''.

'''javascript
return Q.all([
    eventualAdd(2, 2),
    eventualAdd(10, 20)
]);
'''

If you have a promise for an array, you can use ''spread'' as a
replacement for ''then''.  The ''spread'' function “spreads” the
...
```

#### <a name="apidoc.element.q.Promise.race"></a>[function <span class="apidocSignatureSpan">q.Promise.</span>race (answerPs)](#apidoc.element.q.Promise.race)
- description and source-code
```javascript
function race(answerPs) {
    return promise(function (resolve, reject) {
        // Switch to this once we can assume at least ES5
        // answerPs.forEach(function (answerP) {
        //     Q(answerP).then(resolve, reject);
        // });
        // Use this in the meantime
        for (var i = 0, len = answerPs.length; i < len; i++) {
            Q(answerPs[i]).then(resolve, reject);
        }
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.Promise.reject"></a>[function <span class="apidocSignatureSpan">q.Promise.</span>reject (reason)](#apidoc.element.q.Promise.reject)
- description and source-code
```javascript
function reject(reason) {
    var rejection = Promise({
        "when": function (rejected) {
            // note that the error has been handled
            if (rejected) {
                untrackRejection(this);
            }
            return rejected ? rejected(reason) : this;
        }
    }, function fallback() {
        return this;
    }, function inspect() {
        return { state: "rejected", reason: reason };
    });

    // Note that the reason has not been handled.
    trackRejection(rejection, reason);

    return rejection;
}
```
- example usage
```shell
...
instead of promise-based, Q provides a few shortcuts (like ''Q.nfcall'' and
friends). But much of the time, the solution will be to use *deferreds*.

'''javascript
var deferred = Q.defer();
FS.readFile("foo.txt", "utf-8", function (error, text) {
    if (error) {
        deferred.reject(new Error(error));
    } else {
        deferred.resolve(text);
    }
});
return deferred.promise;
'''
...
```

#### <a name="apidoc.element.q.Promise.resolve"></a>[function <span class="apidocSignatureSpan">q.Promise.</span>resolve (value)](#apidoc.element.q.Promise.resolve)
- description and source-code
```javascript
function Q(value) {
    // If the object is already a Promise, return it directly.  This enables
    // the resolve function to both be used to created references from objects,
    // but to tolerably coerce non-promises to promises.
    if (value instanceof Promise) {
        return value;
    }

    // assimilate thenables
    if (isPromiseAlike(value)) {
        return coerce(value);
    } else {
        return fulfill(value);
    }
}
```
- example usage
```shell
...

'''javascript
var deferred = Q.defer();
FS.readFile("foo.txt", "utf-8", function (error, text) {
    if (error) {
        deferred.reject(new Error(error));
    } else {
        deferred.resolve(text);
    }
});
return deferred.promise;
'''

Note that a deferred can be resolved with a value or a promise.  The
''reject'' function is a shorthand for resolving with a rejected
...
```



# <a name="apidoc.module.q.defer"></a>[module q.defer](#apidoc.module.q.defer)

#### <a name="apidoc.element.q.defer.defer"></a>[function <span class="apidocSignatureSpan">q.</span>defer ()](#apidoc.element.q.defer.defer)
- description and source-code
```javascript
function defer() {
    // if "messages" is an "Array", that indicates that the promise has not yet
    // been resolved.  If it is "undefined", it has been resolved.  Each
    // element of the messages array is itself an array of complete arguments to
    // forward to the resolved promise.  We coerce the resolution value to a
    // promise using the 'resolve' function because it handles both fully
    // non-thenable values and other thenables gracefully.
    var messages = [], progressListeners = [], resolvedPromise;

    var deferred = object_create(defer.prototype);
    var promise = object_create(Promise.prototype);

    promise.promiseDispatch = function (resolve, op, operands) {
        var args = array_slice(arguments);
        if (messages) {
            messages.push(args);
            if (op === "when" && operands[1]) { // progress operand
                progressListeners.push(operands[1]);
            }
        } else {
            Q.nextTick(function () {
                resolvedPromise.promiseDispatch.apply(resolvedPromise, args);
            });
        }
    };

    // XXX deprecated
    promise.valueOf = function () {
        if (messages) {
            return promise;
        }
        var nearerValue = nearer(resolvedPromise);
        if (isPromise(nearerValue)) {
            resolvedPromise = nearerValue; // shorten chain
        }
        return nearerValue;
    };

    promise.inspect = function () {
        if (!resolvedPromise) {
            return { state: "pending" };
        }
        return resolvedPromise.inspect();
    };

    if (Q.longStackSupport && hasStacks) {
        try {
            throw new Error();
        } catch (e) {
            // NOTE: don't try to use 'Error.captureStackTrace' or transfer the
            // accessor around; that causes memory leaks as per GH-111. Just
            // reify the stack trace as a string ASAP.
            //
            // At the same time, cut off the first line; it's always just
            // "[object Promise]\n", as per the 'toString'.
            promise.stack = e.stack.substring(e.stack.indexOf("\n") + 1);
            promise.stackCounter = longStackCounter++;
        }
    }

    // NOTE: we do the checks for 'resolvedPromise' in each method, instead of
    // consolidating them into 'become', since otherwise we'd create new
    // promises with the lines 'become(whatever(value))'. See e.g. GH-252.

    function become(newPromise) {
        resolvedPromise = newPromise;

        if (Q.longStackSupport && hasStacks) {
            // Only hold a reference to the new promise if long stacks
            // are enabled to reduce memory usage
            promise.source = newPromise;
        }

        array_reduce(messages, function (undefined, message) {
            Q.nextTick(function () {
                newPromise.promiseDispatch.apply(newPromise, message);
            });
        }, void 0);

        messages = void 0;
        progressListeners = void 0;
    }

    deferred.promise = promise;
    deferred.resolve = function (value) {
        if (resolvedPromise) {
            return;
        }

        become(Q(value));
    };

    deferred.fulfill = function (value) {
        if (resolvedPromise) {
            return;
        }

        become(fulfill(value));
    };
    deferred.reject = function (reason) {
        if (resolvedPromise) {
            return;
        }

        become(reject(reason));
    };
    deferred.notify = function (progress) {
        if (resolvedPromise) {
            return;
        }

        array_reduce(progressListeners, function (undefined, progressListener) {
            Q.nextTick(function () {
                progressListener(progress);
            });
        }, void 0);
    };

    return deferred;
}
```
- example usage
```shell
...
#### Using Deferreds

If you have to interface with asynchronous functions that are callback-based
instead of promise-based, Q provides a few shortcuts (like ''Q.nfcall'' and
friends). But much of the time, the solution will be to use *deferreds*.

'''javascript
var deferred = Q.defer();
FS.readFile("foo.txt", "utf-8", function (error, text) {
    if (error) {
        deferred.reject(new Error(error));
    } else {
        deferred.resolve(text);
    }
});
...
```



# <a name="apidoc.module.q.defer.prototype"></a>[module q.defer.prototype](#apidoc.module.q.defer.prototype)

#### <a name="apidoc.element.q.defer.prototype.makeNodeResolver"></a>[function <span class="apidocSignatureSpan">q.defer.prototype.</span>makeNodeResolver ()](#apidoc.element.q.defer.prototype.makeNodeResolver)
- description and source-code
```javascript
makeNodeResolver = function () {
    var self = this;
    return function (error, value) {
        if (error) {
            self.reject(error);
        } else if (arguments.length > 2) {
            self.resolve(array_slice(arguments, 1));
        } else {
            self.resolve(value);
        }
    };
}
```
- example usage
```shell
...
'''

Finally, if you're working with raw deferred objects, there is a
'makeNodeResolver' method on deferreds that can be handy:

'''javascript
var deferred = Q.defer();
FS.readFile("foo.txt", "utf-8", deferred.makeNodeResolver());
return deferred.promise;
'''

### Long Stack Traces

Q comes with optional support for “long stack traces,” wherein the 'stack'
property of 'Error' rejection reasons is rewritten to be traced along
...
```



# <a name="apidoc.module.q.makePromise"></a>[module q.makePromise](#apidoc.module.q.makePromise)

#### <a name="apidoc.element.q.makePromise.makePromise"></a>[function <span class="apidocSignatureSpan">q.</span>makePromise (descriptor, fallback, inspect)](#apidoc.element.q.makePromise.makePromise)
- description and source-code
```javascript
function Promise(descriptor, fallback, inspect) {
    if (fallback === void 0) {
        fallback = function (op) {
            return reject(new Error(
                "Promise does not support operation: " + op
            ));
        };
    }
    if (inspect === void 0) {
        inspect = function () {
            return {state: "unknown"};
        };
    }

    var promise = object_create(Promise.prototype);

    promise.promiseDispatch = function (resolve, op, args) {
        var result;
        try {
            if (descriptor[op]) {
                result = descriptor[op].apply(promise, args);
            } else {
                result = fallback.call(promise, op, args);
            }
        } catch (exception) {
            result = reject(exception);
        }
        if (resolve) {
            resolve(result);
        }
    };

    promise.inspect = inspect;

    // XXX deprecated 'valueOf' and 'exception' support
    if (inspect) {
        var inspected = inspect();
        if (inspected.state === "rejected") {
            promise.exception = inspected.reason;
        }

        promise.valueOf = function () {
            var inspected = inspect();
            if (inspected.state === "pending" ||
                inspected.state === "rejected") {
                return promise;
            }
            return inspected.value;
        };
    }

    return promise;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.q.makePromise.prototype"></a>[module q.makePromise.prototype](#apidoc.module.q.makePromise.prototype)

#### <a name="apidoc.element.q.makePromise.prototype.all"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>all ()](#apidoc.element.q.makePromise.prototype.all)
- description and source-code
```javascript
all = function () {
    return all(this);
}
```
- example usage
```shell
...

### Combination

You can turn an array of promises into a promise for the whole,
fulfilled array using ''all''.

'''javascript
return Q.all([
    eventualAdd(2, 2),
    eventualAdd(10, 20)
]);
'''

If you have a promise for an array, you can use ''spread'' as a
replacement for ''then''.  The ''spread'' function “spreads” the
...
```

#### <a name="apidoc.element.q.makePromise.prototype.allResolved"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>allResolved ()](#apidoc.element.q.makePromise.prototype.allResolved)
- description and source-code
```javascript
allResolved = function () {
    return allResolved(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.allSettled"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>allSettled ()](#apidoc.element.q.makePromise.prototype.allSettled)
- description and source-code
```javascript
allSettled = function () {
    return this.then(function (promises) {
        return all(array_map(promises, function (promise) {
            promise = Q(promise);
            function regardless() {
                return promise.inspect();
            }
            return promise.then(regardless, regardless);
        }));
    });
}
```
- example usage
```shell
...
promise is fulfilled, the array contains the fulfillment values of the original
promises, in the same order as those promises.  If one of the given promises
is rejected, the returned promise is immediately rejected, not waiting for the
rest of the batch.  If you want to wait for all of the promises to either be
fulfilled or rejected, you can use ''allSettled''.

'''javascript
Q.allSettled(promises)
.then(function (results) {
results.forEach(function (result) {
    if (result.state === "fulfilled") {
        var value = result.value;
    } else {
        var reason = result.reason;
    }
...
```

#### <a name="apidoc.element.q.makePromise.prototype.any"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>any ()](#apidoc.element.q.makePromise.prototype.any)
- description and source-code
```javascript
any = function () {
    return any(this);
}
```
- example usage
```shell
...
'''

The ''any'' function accepts an array of promises and returns a promise that is
fulfilled by the first given promise to be fulfilled, or rejected if all of the
given promises are rejected.

'''javascript
Q.any(promises)
.then(function (first) {
    // Any of the promises was fulfilled.
}, function (error) {
    // All of the promises were rejected.
});
'''
...
```

#### <a name="apidoc.element.q.makePromise.prototype.catch"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>catch (rejected)](#apidoc.element.q.makePromise.prototype.catch)
- description and source-code
```javascript
catch = function (rejected) {
    return this.then(void 0, rejected);
}
```
- example usage
```shell
...
Q.fcall(promisedStep1)
.then(promisedStep2)
.then(promisedStep3)
.then(promisedStep4)
.then(function (value4) {
    // Do something with value4
})
.catch(function (error) {
    // Handle any error from all above steps
})
.done();
'''

With this approach, you also get implicit error propagation, just like 'try',
'catch', and 'finally'.  An error in 'promisedStep1' will flow all the way to
...
```

#### <a name="apidoc.element.q.makePromise.prototype.del"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>del (key)](#apidoc.element.q.makePromise.prototype.del)
- description and source-code
```javascript
del = function (key) {
    return this.dispatch("delete", [key]);
}
```
- example usage
```shell
...
promises, so they can be chained.

'''
direct manipulation         using a promise as a proxy
--------------------------  -------------------------------
value.foo                   promise.get("foo")
value.foo = value           promise.put("foo", value)
delete value.foo            promise.del("foo")
value.foo(...args)          promise.post("foo", [args])
value.foo(...args)          promise.invoke("foo", ...args)
value(...args)              promise.fapply([args])
value(...args)              promise.fcall(...args)
'''

If the promise is a proxy for a remote object, you can shave
...
```

#### <a name="apidoc.element.q.makePromise.prototype.delay"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>delay (timeout)](#apidoc.element.q.makePromise.prototype.delay)
- description and source-code
```javascript
delay = function (timeout) {
    return this.then(function (value) {
        var deferred = defer();
        setTimeout(function () {
            deferred.resolve(value);
        }, timeout);
        return deferred.promise;
    });
}
```
- example usage
```shell
...

Q comes with optional support for “long stack traces,” wherein the 'stack'
property of 'Error' rejection reasons is rewritten to be traced along
asynchronous jumps instead of stopping at the most recent one. As an example:

'''js
function theDepthsOfMyProgram() {
  Q.delay(100).done(function explode() {
    throw new Error("boo!");
  });
}

theDepthsOfMyProgram();
'''
...
```

#### <a name="apidoc.element.q.makePromise.prototype.delete"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>delete (key)](#apidoc.element.q.makePromise.prototype.delete)
- description and source-code
```javascript
delete = function (key) {
    return this.dispatch("delete", [key]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.denodeify"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>denodeify ()](#apidoc.element.q.makePromise.prototype.denodeify)
- description and source-code
```javascript
denodeify = function () {
    var args = array_slice(arguments);
    args.unshift(this);
    return Q.denodeify.apply(void 0, args);
}
```
- example usage
```shell
...
return Q.ninvoke(redisClient, "get", "user:1:id");
return Q.npost(redisClient, "get", ["user:1:id"]);
'''

You can also create reusable wrappers with 'Q.denodeify' or 'Q.nbind':

'''javascript
var readFile = Q.denodeify(FS.readFile);
return readFile("foo.txt", "utf-8");

var redisClientGet = Q.nbind(redisClient.get, redisClient);
return redisClientGet("user:1:id");
'''

Finally, if you're working with raw deferred objects, there is a
...
```

#### <a name="apidoc.element.q.makePromise.prototype.dispatch"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>dispatch (op, args)](#apidoc.element.q.makePromise.prototype.dispatch)
- description and source-code
```javascript
dispatch = function (op, args) {
    var self = this;
    var deferred = defer();
    Q.nextTick(function () {
        self.promiseDispatch(deferred.resolve, op, args);
    });
    return deferred.promise;
}
```
- example usage
```shell
...
 * @param object* the recipient
 * @param op the name of the message operation, e.g., "when",
 * @param args further arguments to be forwarded to the operation
 * @returns result {Promise} a promise for the result of the operation
 */
Q.dispatch = dispatch;
function dispatch(object, op, args) {
return Q(object).dispatch(op, args);
}

Promise.prototype.dispatch = function (op, args) {
var self = this;
var deferred = defer();
Q.nextTick(function () {
    self.promiseDispatch(deferred.resolve, op, args);
...
```

#### <a name="apidoc.element.q.makePromise.prototype.done"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>done (fulfilled, rejected, progress)](#apidoc.element.q.makePromise.prototype.done)
- description and source-code
```javascript
done = function (fulfilled, rejected, progress) {
    var onUnhandledError = function (error) {
        // forward to a future turn so that ''when''
        // does not catch it and turn it into a rejection.
        Q.nextTick(function () {
            makeStackTraceLong(error, promise);
            if (Q.onerror) {
                Q.onerror(error);
            } else {
                throw error;
            }
        });
    };

    // Avoid unnecessary 'nextTick'ing via an unnecessary 'when'.
    var promise = fulfilled || rejected || progress ?
        this.then(fulfilled, rejected, progress) :
        this;

    if (typeof process === "object" && process && process.domain) {
        onUnhandledError = process.domain.bind(onUnhandledError);
    }

    promise.then(void 0, onUnhandledError);
}
```
- example usage
```shell
...
.then(promisedStep4)
.then(function (value4) {
    // Do something with value4
})
.catch(function (error) {
    // Handle any error from all above steps
})
.done();
'''

With this approach, you also get implicit error propagation, just like 'try',
'catch', and 'finally'.  An error in 'promisedStep1' will flow all the way to
the 'catch' function, where it’s caught and handled.  (Here 'promisedStepN' is
a version of 'stepN' that returns a promise.)
...
```

#### <a name="apidoc.element.q.makePromise.prototype.fail"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fail (rejected)](#apidoc.element.q.makePromise.prototype.fail)
- description and source-code
```javascript
fail = function (rejected) {
    return this.then(void 0, rejected);
}
```
- example usage
```shell
...
'''

Q promises provide a ''fail'' shorthand for ''then'' when you are only
interested in handling the error:

'''javascript
var outputPromise = getInputPromise()
.fail(function (error) {
});
'''

If you are writing JavaScript for modern engines only or using
CoffeeScript, you may use 'catch' instead of 'fail'.

Promises also have a ''fin'' function that is like a ''finally'' clause.
...
```

#### <a name="apidoc.element.q.makePromise.prototype.fapply"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fapply (args)](#apidoc.element.q.makePromise.prototype.fapply)
- description and source-code
```javascript
fapply = function (args) {
    return this.dispatch("apply", [void 0, args]);
}
```
- example usage
```shell
...
direct manipulation         using a promise as a proxy
--------------------------  -------------------------------
value.foo                   promise.get("foo")
value.foo = value           promise.put("foo", value)
delete value.foo            promise.del("foo")
value.foo(...args)          promise.post("foo", [args])
value.foo(...args)          promise.invoke("foo", ...args)
value(...args)              promise.fapply([args])
value(...args)              promise.fcall(...args)
'''

If the promise is a proxy for a remote object, you can shave
round-trips by using these functions instead of ''then''.  To take
advantage of promises for remote objects, check out [Q-Connection][].
...
```

#### <a name="apidoc.element.q.makePromise.prototype.fbind"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fbind ()](#apidoc.element.q.makePromise.prototype.fbind)
- description and source-code
```javascript
fbind = function () {
    var promise = this;
    var args = array_slice(arguments);
    return function fbound() {
        return promise.dispatch("apply", [
            this,
            args.concat(array_slice(arguments))
        ]);
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.fcall"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fcall ()](#apidoc.element.q.makePromise.prototype.fcall)
- description and source-code
```javascript
fcall = function () {
    return this.dispatch("apply", [void 0, array_slice(arguments)]);
}
```
- example usage
```shell
...
    });
});
'''

With a promise library, you can flatten the pyramid.

'''javascript
Q.fcall(promisedStep1)
.then(promisedStep2)
.then(promisedStep3)
.then(promisedStep4)
.then(function (value4) {
    // Do something with value4
})
.catch(function (error) {
...
```

#### <a name="apidoc.element.q.makePromise.prototype.fin"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>fin (callback)](#apidoc.element.q.makePromise.prototype.fin)
- description and source-code
```javascript
fin = function (callback) {
    if (!callback || typeof callback.apply !== "function") {
        throw new Error("Q can't apply finally callback");
    }
    callback = Q(callback);
    return this.then(function (value) {
        return callback.fcall().then(function () {
            return value;
        });
    }, function (reason) {
        // TODO attempt to recycle the rejection with "this".
        return callback.fcall().then(function () {
            throw reason;
        });
    });
}
```
- example usage
```shell
...
returned by ''getInputPromise()'' either returns a value or throws an
error.  The value returned or error thrown by ''getInputPromise()''
passes directly to ''outputPromise'' unless the final handler fails, and
may be delayed if the final handler returns a promise.

'''javascript
var outputPromise = getInputPromise()
.fin(function () {
    // close files, database connections, stop servers, conclude tests
});
'''

-   If the handler returns a value, the value is ignored
-   If the handler throws an error, the error passes to ''outputPromise''
-   If the handler returns a promise, ''outputPromise'' gets postponed.  The
...
```

#### <a name="apidoc.element.q.makePromise.prototype.finally"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>finally (callback)](#apidoc.element.q.makePromise.prototype.finally)
- description and source-code
```javascript
finally = function (callback) {
    if (!callback || typeof callback.apply !== "function") {
        throw new Error("Q can't apply finally callback");
    }
    callback = Q(callback);
    return this.then(function (value) {
        return callback.fcall().then(function () {
            return value;
        });
    }, function (reason) {
        // TODO attempt to recycle the rejection with "this".
        return callback.fcall().then(function () {
            throw reason;
        });
    });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.get"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>get (key)](#apidoc.element.q.makePromise.prototype.get)
- description and source-code
```javascript
get = function (key) {
    return this.dispatch("get", [key]);
}
```
- example usage
```shell
...
object.  There are methods that allow you to optimistically manipulate
properties or call functions.  All of these interactions return
promises, so they can be chained.

'''
direct manipulation         using a promise as a proxy
--------------------------  -------------------------------
value.foo                   promise.get("foo")
value.foo = value           promise.put("foo", value)
delete value.foo            promise.del("foo")
value.foo(...args)          promise.post("foo", [args])
value.foo(...args)          promise.invoke("foo", ...args)
value(...args)              promise.fapply([args])
value(...args)              promise.fcall(...args)
'''
...
```

#### <a name="apidoc.element.q.makePromise.prototype.invoke"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>invoke (name)](#apidoc.element.q.makePromise.prototype.invoke)
- description and source-code
```javascript
invoke = function (name) {
    return this.dispatch("post", [name, array_slice(arguments, 1)]);
}
```
- example usage
```shell
...
'''

If there is any chance that the promise you receive is not a Q promise
as provided by your library, you should wrap it using a Q function.
You can even use ''Q.invoke'' as a shorthand.

'''javascript
return Q.invoke($, 'ajax', ...)
.then(function () {
});
'''


### Over the Wire
...
```

#### <a name="apidoc.element.q.makePromise.prototype.isFulfilled"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>isFulfilled ()](#apidoc.element.q.makePromise.prototype.isFulfilled)
- description and source-code
```javascript
isFulfilled = function () {
    return this.inspect().state === "fulfilled";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.isPending"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>isPending ()](#apidoc.element.q.makePromise.prototype.isPending)
- description and source-code
```javascript
isPending = function () {
    return this.inspect().state === "pending";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.isRejected"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>isRejected ()](#apidoc.element.q.makePromise.prototype.isRejected)
- description and source-code
```javascript
isRejected = function () {
    return this.inspect().state === "rejected";
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.join"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>join (that)](#apidoc.element.q.makePromise.prototype.join)
- description and source-code
```javascript
join = function (that) {
    return Q([this, that]).spread(function (x, y) {
        if (x === y) {
            // TODO: "===" should be Object.is or equiv
            return x;
        } else {
            throw new Error("Q can't join: not the same: " + x + " " + y);
        }
    });
}
```
- example usage
```shell
...
        if (p.stack && (!error.__minimumStackCounter__ || error.__minimumStackCounter__ > p.stackCounter)) {
            object_defineProperty(error, "__minimumStackCounter__", {value: p.stackCounter, configurable: true});
            stacks.unshift(p.stack);
        }
    }
    stacks.unshift(error.stack);

    var concatedStacks = stacks.join("\n" + STACK_JUMP_SEPARATOR + "\n");
    var stack = filterStackString(concatedStacks);
    object_defineProperty(error, "stack", {value: stack, configurable: true});
}
}

function filterStackString(stackString) {
var lines = stackString.split("\n");
...
```

#### <a name="apidoc.element.q.makePromise.prototype.keys"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>keys ()](#apidoc.element.q.makePromise.prototype.keys)
- description and source-code
```javascript
keys = function () {
    return this.dispatch("keys", []);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.mapply"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>mapply (name, args)](#apidoc.element.q.makePromise.prototype.mapply)
- description and source-code
```javascript
mapply = function (name, args) {
    return this.dispatch("post", [name, args]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.mcall"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>mcall (name)](#apidoc.element.q.makePromise.prototype.mcall)
- description and source-code
```javascript
mcall = function (name) {
    return this.dispatch("post", [name, array_slice(arguments, 1)]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.nbind"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nbind ()](#apidoc.element.q.makePromise.prototype.nbind)
- description and source-code
```javascript
nbind = function () {
    var args = array_slice(arguments, 0);
    args.unshift(this);
    return Q.nbind.apply(void 0, args);
}
```
- example usage
```shell
...

You can also create reusable wrappers with 'Q.denodeify' or 'Q.nbind':

'''javascript
var readFile = Q.denodeify(FS.readFile);
return readFile("foo.txt", "utf-8");

var redisClientGet = Q.nbind(redisClient.get, redisClient);
return redisClientGet("user:1:id");
'''

Finally, if you're working with raw deferred objects, there is a
'makeNodeResolver' method on deferreds that can be handy:

'''javascript
...
```

#### <a name="apidoc.element.q.makePromise.prototype.nfapply"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nfapply (args)](#apidoc.element.q.makePromise.prototype.nfapply)
- description and source-code
```javascript
nfapply = function (args) {
    var deferred = defer();
    var nodeArgs = array_slice(args);
    nodeArgs.push(deferred.makeNodeResolver());
    this.fapply(nodeArgs).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
...
where callbacks are in the form of 'function(err, result)', Q provides a few
useful utility functions for converting between them. The most straightforward
are probably 'Q.nfcall' and 'Q.nfapply' ("Node function call/apply") for calling
Node.js-style functions and getting back a promise:

'''javascript
return Q.nfcall(FS.readFile, "foo.txt", "utf-8");
return Q.nfapply(FS.readFile, ["foo.txt", "utf-8"]);
'''

If you are working with methods, instead of simple functions, you can easily
run in to the usual problems where passing a method to another function—like
'Q.nfcall'—"un-binds" the method from its owner. To avoid this, you can either
use 'Function.prototype.bind' or some nice shortcut methods we provide:
...
```

#### <a name="apidoc.element.q.makePromise.prototype.nfbind"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nfbind ()](#apidoc.element.q.makePromise.prototype.nfbind)
- description and source-code
```javascript
nfbind = function () {
    var args = array_slice(arguments);
    args.unshift(this);
    return Q.denodeify.apply(void 0, args);
}
```
- example usage
```shell
...
return deferred.promise;
};

/**
 * Wraps a NodeJS continuation passing function and returns an equivalent
 * version that returns a promise.
 * @example
 * Q.nfbind(FS.readFile, __filename)("utf-8")
 * .then(console.log)
 * .done()
 */
Q.nfbind =
Q.denodeify = function (callback /*...args*/) {
if (callback === undefined) {
    throw new Error("Q can't wrap an undefined function");
...
```

#### <a name="apidoc.element.q.makePromise.prototype.nfcall"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nfcall ()](#apidoc.element.q.makePromise.prototype.nfcall)
- description and source-code
```javascript
nfcall = function () {
    var nodeArgs = array_slice(arguments);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    this.fapply(nodeArgs).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
...
If you're working with functions that make use of the Node.js callback pattern,
where callbacks are in the form of 'function(err, result)', Q provides a few
useful utility functions for converting between them. The most straightforward
are probably 'Q.nfcall' and 'Q.nfapply' ("Node function call/apply") for calling
Node.js-style functions and getting back a promise:

'''javascript
return Q.nfcall(FS.readFile, "foo.txt", "utf-8");
return Q.nfapply(FS.readFile, ["foo.txt", "utf-8"]);
'''

If you are working with methods, instead of simple functions, you can easily
run in to the usual problems where passing a method to another function—like
'Q.nfcall'—"un-binds" the method from its owner. To avoid this, you can either
use 'Function.prototype.bind' or some nice shortcut methods we provide:
...
```

#### <a name="apidoc.element.q.makePromise.prototype.ninvoke"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>ninvoke (name)](#apidoc.element.q.makePromise.prototype.ninvoke)
- description and source-code
```javascript
ninvoke = function (name) {
    var nodeArgs = array_slice(arguments, 1);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    this.dispatch("post", [name, nodeArgs]).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
...

If you are working with methods, instead of simple functions, you can easily
run in to the usual problems where passing a method to another function—like
'Q.nfcall'—"un-binds" the method from its owner. To avoid this, you can either
use 'Function.prototype.bind' or some nice shortcut methods we provide:

'''javascript
return Q.ninvoke(redisClient, "get", "user:1:id");
return Q.npost(redisClient, "get", ["user:1:id"]);
'''

You can also create reusable wrappers with 'Q.denodeify' or 'Q.nbind':

'''javascript
var readFile = Q.denodeify(FS.readFile);
...
```

#### <a name="apidoc.element.q.makePromise.prototype.nmapply"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nmapply (name, args)](#apidoc.element.q.makePromise.prototype.nmapply)
- description and source-code
```javascript
nmapply = function (name, args) {
    var nodeArgs = array_slice(args || []);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    this.dispatch("post", [name, nodeArgs]).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.nmcall"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nmcall (name)](#apidoc.element.q.makePromise.prototype.nmcall)
- description and source-code
```javascript
nmcall = function (name) {
    var nodeArgs = array_slice(arguments, 1);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    this.dispatch("post", [name, nodeArgs]).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.nodeify"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nodeify (nodeback)](#apidoc.element.q.makePromise.prototype.nodeify)
- description and source-code
```javascript
nodeify = function (nodeback) {
    if (nodeback) {
        this.then(function (value) {
            Q.nextTick(function () {
                nodeback(null, value);
            });
        }, function (error) {
            Q.nextTick(function () {
                nodeback(error);
            });
        });
    } else {
        return this;
    }
}
```
- example usage
```shell
...
 * pass a nodeback, they will receive the result promise.
 * @param object a result (or a promise for a result)
 * @param {Function} nodeback a Node.js-style callback
 * @returns either the promise or nothing
 */
Q.nodeify = nodeify;
function nodeify(object, nodeback) {
return Q(object).nodeify(nodeback);
}

Promise.prototype.nodeify = function (nodeback) {
if (nodeback) {
    this.then(function (value) {
        Q.nextTick(function () {
            nodeback(null, value);
...
```

#### <a name="apidoc.element.q.makePromise.prototype.npost"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>npost (name, args)](#apidoc.element.q.makePromise.prototype.npost)
- description and source-code
```javascript
npost = function (name, args) {
    var nodeArgs = array_slice(args || []);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    this.dispatch("post", [name, nodeArgs]).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
...
If you are working with methods, instead of simple functions, you can easily
run in to the usual problems where passing a method to another function—like
'Q.nfcall'—"un-binds" the method from its owner. To avoid this, you can either
use 'Function.prototype.bind' or some nice shortcut methods we provide:

'''javascript
return Q.ninvoke(redisClient, "get", "user:1:id");
return Q.npost(redisClient, "get", ["user:1:id"]);
'''

You can also create reusable wrappers with 'Q.denodeify' or 'Q.nbind':

'''javascript
var readFile = Q.denodeify(FS.readFile);
return readFile("foo.txt", "utf-8");
...
```

#### <a name="apidoc.element.q.makePromise.prototype.nsend"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>nsend (name)](#apidoc.element.q.makePromise.prototype.nsend)
- description and source-code
```javascript
nsend = function (name) {
    var nodeArgs = array_slice(arguments, 1);
    var deferred = defer();
    nodeArgs.push(deferred.makeNodeResolver());
    this.dispatch("post", [name, nodeArgs]).fail(deferred.reject);
    return deferred.promise;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.passByCopy"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>passByCopy ()](#apidoc.element.q.makePromise.prototype.passByCopy)
- description and source-code
```javascript
passByCopy = function () {
    //freeze(object);
    //passByCopies.set(object, true);
    return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.post"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>post (name, args)](#apidoc.element.q.makePromise.prototype.post)
- description and source-code
```javascript
post = function (name, args) {
    return this.dispatch("post", [name, args]);
}
```
- example usage
```shell
...

'''
direct manipulation         using a promise as a proxy
--------------------------  -------------------------------
value.foo                   promise.get("foo")
value.foo = value           promise.put("foo", value)
delete value.foo            promise.del("foo")
value.foo(...args)          promise.post("foo", [args])
value.foo(...args)          promise.invoke("foo", ...args)
value(...args)              promise.fapply([args])
value(...args)              promise.fcall(...args)
'''

If the promise is a proxy for a remote object, you can shave
round-trips by using these functions instead of ''then''.  To take
...
```

#### <a name="apidoc.element.q.makePromise.prototype.progress"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>progress (progressed)](#apidoc.element.q.makePromise.prototype.progress)
- description and source-code
```javascript
progress = function (progressed) {
    return this.then(void 0, void 0, progressed);
}
```
- example usage
```shell
...
});
'''

Like 'fail', Q also provides a shorthand for progress callbacks
called 'progress':

'''javascript
return uploadFile().progress(function (progress) {
    // We get notified of the upload's progress
});
'''

### The End

When you get to the end of a chain of promises, you should either
...
```

#### <a name="apidoc.element.q.makePromise.prototype.race"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>race ()](#apidoc.element.q.makePromise.prototype.race)
- description and source-code
```javascript
race = function () {
    return this.then(Q.race);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.q.makePromise.prototype.send"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>send (name)](#apidoc.element.q.makePromise.prototype.send)
- description and source-code
```javascript
send = function (name) {
    return this.dispatch("post", [name, array_slice(arguments, 1)]);
}
```
- example usage
```shell
...
var request = new XMLHttpRequest();
var deferred = Q.defer();

request.open("GET", url, true);
request.onload = onload;
request.onerror = onerror;
request.onprogress = onprogress;
request.send();

function onload() {
    if (request.status === 200) {
        deferred.resolve(request.responseText);
    } else {
        deferred.reject(new Error("Status code was " + request.status));
    }
...
```

#### <a name="apidoc.element.q.makePromise.prototype.set"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>set (key, value)](#apidoc.element.q.makePromise.prototype.set)
- description and source-code
```javascript
set = function (key, value) {
    return this.dispatch("set", [key, value]);
}
```
- example usage
```shell
...
promise.resolve = Q; // ES6

// XXX experimental.  This method is a way to denote that a local value is
// serializable and should be immediately dispatched to a remote upon request,
// instead of passing a reference.
Q.passByCopy = function (object) {
//freeze(object);
//passByCopies.set(object, true);
return object;
};

Promise.prototype.passByCopy = function () {
//freeze(object);
//passByCopies.set(object, true);
return this;
...
```

#### <a name="apidoc.element.q.makePromise.prototype.spread"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>spread (fulfilled, rejected)](#apidoc.element.q.makePromise.prototype.spread)
- description and source-code
```javascript
spread = function (fulfilled, rejected) {
    return this.all().then(function (array) {
        return fulfilled.apply(void 0, array);
    }, rejected);
}
```
- example usage
```shell
...
replacement for ''then''.  The ''spread'' function “spreads” the
values over the arguments of the fulfillment handler.  The rejection handler
will get called at the first sign of failure.  That is, whichever of
the received promises fails first gets handled by the rejection handler.

'''javascript
function eventualAdd(a, b) {
    return Q.spread([a, b], function (a, b) {
        return a + b;
    })
}
'''

But ''spread'' calls ''all'' initially, so you can skip it in chains.
...
```

#### <a name="apidoc.element.q.makePromise.prototype.tap"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>tap (callback)](#apidoc.element.q.makePromise.prototype.tap)
- description and source-code
```javascript
tap = function (callback) {
    callback = Q(callback);

    return this.then(function (value) {
        return callback.fcall(value).thenResolve(value);
    });
}
```
- example usage
```shell
...
       }
   }]);

   return deferred.promise;
};

Q.tap = function (promise, callback) {
   return Q(promise).tap(callback);
};

/**
* Works almost like "finally", but not called for rejections.
* Original resolution value is passed through callback unaffected.
* Callback may return a promise that will be awaited for.
* @param {Function} callback
...
```

#### <a name="apidoc.element.q.makePromise.prototype.then"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>then (fulfilled, rejected, progressed)](#apidoc.element.q.makePromise.prototype.then)
- description and source-code
```javascript
then = function (fulfilled, rejected, progressed) {
    var self = this;
    var deferred = defer();
    var done = false;   // ensure the untrusted promise makes at most a
                        // single call to one of the callbacks

    function _fulfilled(value) {
        try {
            return typeof fulfilled === "function" ? fulfilled(value) : value;
        } catch (exception) {
            return reject(exception);
        }
    }

    function _rejected(exception) {
        if (typeof rejected === "function") {
            makeStackTraceLong(exception, self);
            try {
                return rejected(exception);
            } catch (newException) {
                return reject(newException);
            }
        }
        return reject(exception);
    }

    function _progressed(value) {
        return typeof progressed === "function" ? progressed(value) : value;
    }

    Q.nextTick(function () {
        self.promiseDispatch(function (value) {
            if (done) {
                return;
            }
            done = true;

            deferred.resolve(_fulfilled(value));
        }, "when", [function (exception) {
            if (done) {
                return;
            }
            done = true;

            deferred.resolve(_rejected(exception));
        }]);
    });

    // Progress propagator need to be attached in the current tick.
    self.promiseDispatch(void 0, "when", [void 0, function (value) {
        var newValue;
        var threw = false;
        try {
            newValue = _progressed(value);
        } catch (e) {
            threw = true;
            if (Q.onerror) {
                Q.onerror(e);
            } else {
                throw e;
            }
        }

        if (!threw) {
            deferred.notify(newValue);
        }
    }]);

    return deferred.promise;
}
```
- example usage
```shell
...
});
'''

With a promise library, you can flatten the pyramid.

'''javascript
Q.fcall(promisedStep1)
.then(promisedStep2)
.then(promisedStep3)
.then(promisedStep4)
.then(function (value4) {
// Do something with value4
})
.catch(function (error) {
// Handle any error from all above steps
...
```

#### <a name="apidoc.element.q.makePromise.prototype.thenReject"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>thenReject (reason)](#apidoc.element.q.makePromise.prototype.thenReject)
- description and source-code
```javascript
thenReject = function (reason) {
    return this.then(function () { throw reason; });
}
```
- example usage
```shell
...
};

Promise.prototype.thenReject = function (reason) {
   return this.then(function () { throw reason; });
};

Q.thenReject = function (promise, reason) {
   return Q(promise).thenReject(reason);
};

/**
* If an object is not a promise, it is as "near" as possible.
* If a promise is rejected, it is as "near" as possible too.
* If it’s a fulfilled promise, the fulfillment value is nearer.
* If it’s a deferred promise and the deferred has been resolved, the
...
```

#### <a name="apidoc.element.q.makePromise.prototype.thenResolve"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>thenResolve (value)](#apidoc.element.q.makePromise.prototype.thenResolve)
- description and source-code
```javascript
thenResolve = function (value) {
    return this.then(function () { return value; });
}
```
- example usage
```shell
...
*   .tap(console.log)
*   .then(...);
*/
Promise.prototype.tap = function (callback) {
   callback = Q(callback);

   return this.then(function (value) {
       return callback.fcall(value).thenResolve(value);
   });
};

/**
* Registers an observer on a promise.
*
* Guarantees:
...
```

#### <a name="apidoc.element.q.makePromise.prototype.timeout"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>timeout (ms, error)](#apidoc.element.q.makePromise.prototype.timeout)
- description and source-code
```javascript
timeout = function (ms, error) {
    var deferred = defer();
    var timeoutId = setTimeout(function () {
        if (!error || "string" === typeof error) {
            error = new Error(error || "Timed out after " + ms + " ms");
            error.code = "ETIMEDOUT";
        }
        deferred.reject(error);
    }, ms);

    this.then(function (value) {
        clearTimeout(timeoutId);
        deferred.resolve(value);
    }, function (exception) {
        clearTimeout(timeoutId);
        deferred.reject(exception);
    }, deferred.notify);

    return deferred.promise;
}
```
- example usage
```shell
...
 * @param {Any*} promise
 * @param {Number} milliseconds timeout
 * @param {Any*} custom error message or Error object (optional)
 * @returns a promise for the resolution of the given promise if it is
 * fulfilled before the timeout, otherwise rejected.
 */
Q.timeout = function (object, ms, error) {
return Q(object).timeout(ms, error);
};

Promise.prototype.timeout = function (ms, error) {
var deferred = defer();
var timeoutId = setTimeout(function () {
    if (!error || "string" === typeof error) {
        error = new Error(error || "Timed out after " + ms + " ms");
...
```

#### <a name="apidoc.element.q.makePromise.prototype.toString"></a>[function <span class="apidocSignatureSpan">q.makePromise.prototype.</span>toString ()](#apidoc.element.q.makePromise.prototype.toString)
- description and source-code
```javascript
toString = function () {
    return "[object Promise]";
}
```
- example usage
```shell
...
    if (!flushing) {
        flushing = true;
        requestTick();
    }
};

if (typeof process === "object" &&
    process.toString() === "[object process]" && process.nextTick) {
    // Ensure Q is in a real Node environment, with a 'process.nextTick'.
    // To see through fake Node environments:
    // * Mocha test runner - exposes a 'process' global without a 'nextTick'
    // * Browserify - exposes a 'process.nexTick' function that uses
    //   'setTimeout'. In this case 'setImmediate' is preferred because
    //    it is faster. Browserify's 'process.toString()' yields
    //   "[object Object]", while in a real Node environment
...
```



# <a name="apidoc.module.q.nextTick"></a>[module q.nextTick](#apidoc.module.q.nextTick)

#### <a name="apidoc.element.q.nextTick.nextTick"></a>[function <span class="apidocSignatureSpan">q.</span>nextTick (task)](#apidoc.element.q.nextTick.nextTick)
- description and source-code
```javascript
nextTick = function (task) {
    tail = tail.next = {
        task: task,
        domain: isNodeJS && process.domain,
        next: null
    };

    if (!flushing) {
        flushing = true;
        requestTick();
    }
}
```
- example usage
```shell
...
    //   'setTimeout'. In this case 'setImmediate' is preferred because
    //    it is faster. Browserify's 'process.toString()' yields
    //   "[object Object]", while in a real Node environment
    //   'process.toString()' yields "[object process]".
    isNodeJS = true;

    requestTick = function () {
        process.nextTick(flush);
    };

} else if (typeof setImmediate === "function") {
    // In IE10, Node.js 0.9+, or https://github.com/NobleJS/setImmediate
    if (typeof window !== "undefined") {
        requestTick = setImmediate.bind(window, flush);
    } else {
...
```

#### <a name="apidoc.element.q.nextTick.runAfter"></a>[function <span class="apidocSignatureSpan">q.nextTick.</span>runAfter (task)](#apidoc.element.q.nextTick.runAfter)
- description and source-code
```javascript
runAfter = function (task) {
    laterQueue.push(task);
    if (!flushing) {
        flushing = true;
        requestTick();
    }
}
```
- example usage
```shell
...
}

function trackRejection(promise, reason) {
if (!trackUnhandledRejections) {
    return;
}
if (typeof process === "object" && typeof process.emit === "function") {
    Q.nextTick.runAfter(function () {
        if (array_indexOf(unhandledRejections, promise) !== -1) {
            process.emit("unhandledRejection", reason, promise);
            reportedUnhandledRejections.push(promise);
        }
    });
}
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
