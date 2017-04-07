# api documentation for  [maildev (v0.14.0)](http://djfarrelly.github.io/MailDev/)  [![npm package](https://img.shields.io/npm/v/npmdoc-maildev.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-maildev) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-maildev.svg)](https://travis-ci.org/npmdoc/node-npmdoc-maildev)
#### SMTP Server and Web Interface for reading and testing emails during development

[![NPM](https://nodei.co/npm/maildev.png?downloads=true)](https://www.npmjs.com/package/maildev)

[![apidoc](https://npmdoc.github.io/node-npmdoc-maildev/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-maildev_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-maildev/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-maildev/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-maildev/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Dan Farrelly"
    },
    "bin": {
        "maildev": "./bin/maildev"
    },
    "bugs": {
        "url": "https://github.com/djfarrelly/maildev/issues"
    },
    "dependencies": {
        "async": "1.5.1",
        "commander": "2.9.0",
        "express": "4.13.4",
        "mailparser": "0.5.3",
        "open": "0.0.5",
        "simplesmtp": "0.3.35",
        "smtp-connection": "2.3.1",
        "smtp-server": "1.4.0",
        "socket.io": "1.4.5",
        "wildstring": "1.0.8"
    },
    "description": "SMTP Server and Web Interface for reading and testing emails during development",
    "devDependencies": {
        "grunt": "0.4.5",
        "grunt-concurrent": "2.2.1",
        "grunt-contrib-jshint": "1.0.0",
        "grunt-contrib-watch": "1.0.0",
        "grunt-nodemon": "0.4.1",
        "grunt-sass": "1.1.0",
        "http-proxy-middleware": "0.12.0",
        "istanbul": "0.4.4",
        "matchdep": "1.0.1",
        "mocha": "2.2.5",
        "nodemailer": "2.3.0",
        "request": "2.69.0"
    },
    "directories": {},
    "dist": {
        "shasum": "5c0ba72c804a8678f872c4e1a871c849ffa9da22",
        "tarball": "https://registry.npmjs.org/maildev/-/maildev-0.14.0.tgz"
    },
    "engines": {
        "node": ">=0.10.0"
    },
    "gitHead": "4edecfcf1cd7fe173bbe5c78fb9ead71d2756b8e",
    "homepage": "http://djfarrelly.github.io/MailDev/",
    "keywords": [
        "email",
        "e-mail",
        "mail",
        "mailcatcher"
    ],
    "license": "MIT",
    "main": "./index.js",
    "maintainers": [
        {
            "name": "djfarrelly",
            "email": "daniel.j.farrelly@gmail.com"
        }
    ],
    "name": "maildev",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+ssh://git@github.com/djfarrelly/maildev.git"
    },
    "scripts": {
        "test": "istanbul cover _mocha"
    },
    "version": "0.14.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module maildev](#apidoc.module.maildev)
1.  object <span class="apidocSignatureSpan">maildev.</span>logger
1.  object <span class="apidocSignatureSpan">maildev.</span>mailserver
1.  object <span class="apidocSignatureSpan">maildev.</span>outgoing
1.  object <span class="apidocSignatureSpan">maildev.</span>web

#### [module maildev.logger](#apidoc.module.maildev.logger)
1.  [function <span class="apidocSignatureSpan">maildev.logger.</span>dir ()](#apidoc.element.maildev.logger.dir)
1.  [function <span class="apidocSignatureSpan">maildev.logger.</span>error ()](#apidoc.element.maildev.logger.error)
1.  [function <span class="apidocSignatureSpan">maildev.logger.</span>info ()](#apidoc.element.maildev.logger.info)
1.  [function <span class="apidocSignatureSpan">maildev.logger.</span>log ()](#apidoc.element.maildev.logger.log)
1.  [function <span class="apidocSignatureSpan">maildev.logger.</span>setLevel (level)](#apidoc.element.maildev.logger.setLevel)
1.  [function <span class="apidocSignatureSpan">maildev.logger.</span>warn ()](#apidoc.element.maildev.logger.warn)

#### [module maildev.mailserver](#apidoc.module.maildev.mailserver)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>create (port, host, user, password)](#apidoc.element.maildev.mailserver.create)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>deleteAllEmail (done)](#apidoc.element.maildev.mailserver.deleteAllEmail)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>deleteEmail (id, done)](#apidoc.element.maildev.mailserver.deleteEmail)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>emit ()](#apidoc.element.maildev.mailserver.emit)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>end (callback)](#apidoc.element.maildev.mailserver.end)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>getAllEmail (done)](#apidoc.element.maildev.mailserver.getAllEmail)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>getEmail (id, done)](#apidoc.element.maildev.mailserver.getEmail)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>getEmailAttachment (id, filename, done)](#apidoc.element.maildev.mailserver.getEmailAttachment)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>getEmailEml (id, done)](#apidoc.element.maildev.mailserver.getEmailEml)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>getEmailHTML (id, baseUrl, done)](#apidoc.element.maildev.mailserver.getEmailHTML)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>getOutgoingHost ()](#apidoc.element.maildev.mailserver.getOutgoingHost)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>getRawEmail (id, done)](#apidoc.element.maildev.mailserver.getRawEmail)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>isOutgoingEnabled ()](#apidoc.element.maildev.mailserver.isOutgoingEnabled)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>listen (callback)](#apidoc.element.maildev.mailserver.listen)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>on ()](#apidoc.element.maildev.mailserver.on)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>relayMail (idOrMailObject, isAutoRelay, done)](#apidoc.element.maildev.mailserver.relayMail)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>removeAllListeners ()](#apidoc.element.maildev.mailserver.removeAllListeners)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>removeListener ()](#apidoc.element.maildev.mailserver.removeListener)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>setAutoRelayMode (enabled, rules)](#apidoc.element.maildev.mailserver.setAutoRelayMode)
1.  [function <span class="apidocSignatureSpan">maildev.mailserver.</span>setupOutgoing (host, port, user, pass, secure)](#apidoc.element.maildev.mailserver.setupOutgoing)
1.  object <span class="apidocSignatureSpan">maildev.mailserver.</span>store

#### [module maildev.outgoing](#apidoc.module.maildev.outgoing)
1.  [function <span class="apidocSignatureSpan">maildev.outgoing.</span>_createClient ()](#apidoc.element.maildev.outgoing._createClient)
1.  [function <span class="apidocSignatureSpan">maildev.outgoing.</span>close ()](#apidoc.element.maildev.outgoing.close)
1.  [function <span class="apidocSignatureSpan">maildev.outgoing.</span>getOutgoingHost ()](#apidoc.element.maildev.outgoing.getOutgoingHost)
1.  [function <span class="apidocSignatureSpan">maildev.outgoing.</span>isAutoRelayEnabled ()](#apidoc.element.maildev.outgoing.isAutoRelayEnabled)
1.  [function <span class="apidocSignatureSpan">maildev.outgoing.</span>isEnabled ()](#apidoc.element.maildev.outgoing.isEnabled)
1.  [function <span class="apidocSignatureSpan">maildev.outgoing.</span>relayMail (emailObject, emailStream, isAutoRelay, callback)](#apidoc.element.maildev.outgoing.relayMail)
1.  [function <span class="apidocSignatureSpan">maildev.outgoing.</span>setAutoRelayMode (enabled, rules)](#apidoc.element.maildev.outgoing.setAutoRelayMode)
1.  [function <span class="apidocSignatureSpan">maildev.outgoing.</span>setup (host, port, user, pass, secure)](#apidoc.element.maildev.outgoing.setup)

#### [module maildev.web](#apidoc.module.maildev.web)
1.  [function <span class="apidocSignatureSpan">maildev.web.</span>close (callback)](#apidoc.element.maildev.web.close)
1.  [function <span class="apidocSignatureSpan">maildev.web.</span>start (port, host, mailserver, user, password, basePathname)](#apidoc.element.maildev.web.start)



# <a name="apidoc.module.maildev"></a>[module maildev](#apidoc.module.maildev)



# <a name="apidoc.module.maildev.logger"></a>[module maildev.logger](#apidoc.module.maildev.logger)

#### <a name="apidoc.element.maildev.logger.dir"></a>[function <span class="apidocSignatureSpan">maildev.logger.</span>dir ()](#apidoc.element.maildev.logger.dir)
- description and source-code
```javascript
dir = function (){
  if (logLevel > 1) {
    console[ fn ].apply(console, arguments);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maildev.logger.error"></a>[function <span class="apidocSignatureSpan">maildev.logger.</span>error ()](#apidoc.element.maildev.logger.error)
- description and source-code
```javascript
error = function (){
  if (logLevel > 1) {
    console[ fn ].apply(console, arguments);
  }
}
```
- example usage
```shell
...

  store.push(object);

  logger.log('Saving email: ', mailObject.subject);

  if (outgoing.isAutoRelayEnabled()) {
    mailServer.relayMail(object, true, function (err) {
      if (err) logger.error('Error when relaying email', err);
    });
  }

  eventEmitter.emit('new', object);
}

// Save an attachment
...
```

#### <a name="apidoc.element.maildev.logger.info"></a>[function <span class="apidocSignatureSpan">maildev.logger.</span>info ()](#apidoc.element.maildev.logger.info)
- description and source-code
```javascript
info = function () {
  if (logLevel > 0)
    console.info.apply(console, arguments);
}
```
- example usage
```shell
...
  }

  process.on('SIGTERM', function () {
    async.parallel([
      mailserver.end,
      web.close
    ], function(err, results) {
      logger.info('Shutting down...');
      process.exit(0);
    });
  });

  return mailserver;
};
...
```

#### <a name="apidoc.element.maildev.logger.log"></a>[function <span class="apidocSignatureSpan">maildev.logger.</span>log ()](#apidoc.element.maildev.logger.log)
- description and source-code
```javascript
log = function (){
  if (logLevel > 1) {
    console[ fn ].apply(console, arguments);
  }
}
```
- example usage
```shell
...
object.time = new Date();
object.read = false;
object.envelope = envelope;
object.source = path.join(tempDir, id + '.eml');

store.push(object);

logger.log('Saving email: ', mailObject.subject);

if (outgoing.isAutoRelayEnabled()) {
  mailServer.relayMail(object, true, function (err) {
    if (err) logger.error('Error when relaying email', err);
  });
}
...
```

#### <a name="apidoc.element.maildev.logger.setLevel"></a>[function <span class="apidocSignatureSpan">maildev.logger.</span>setLevel (level)](#apidoc.element.maildev.logger.setLevel)
- description and source-code
```javascript
setLevel = function (level) {
  logLevel = level;
}
```
- example usage
```shell
...
    .option('-o, --open', 'Open the Web GUI after startup')
    .option('-v, --verbose')
    .option('--silent')
    .parse(process.argv);
}

if (config.verbose) {
  logger.setLevel(2);
} else if (config.silent) {
  logger.setLevel(0);
}

// Start the Mailserver & Web GUI
mailserver.create(config.smtp, config.ip, config.incomingUser, config.incomingPass);
...
```

#### <a name="apidoc.element.maildev.logger.warn"></a>[function <span class="apidocSignatureSpan">maildev.logger.</span>warn ()](#apidoc.element.maildev.logger.warn)
- description and source-code
```javascript
warn = function (){
  if (logLevel > 1) {
    console[ fn ].apply(console, arguments);
  }
}
```
- example usage
```shell
...
    }
  });

  if (email.attachments){
    deleteAttachments(email.attachments);
  }

  logger.warn('Deleting email - %s', email.subject);

  store.splice(emailIndex, 1);

  done(null, true);
};
...
```



# <a name="apidoc.module.maildev.mailserver"></a>[module maildev.mailserver](#apidoc.module.maildev.mailserver)

#### <a name="apidoc.element.maildev.mailserver.create"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>create (port, host, user, password)](#apidoc.element.maildev.mailserver.create)
- description and source-code
```javascript
create = function (port, host, user, password) {

  // Start the server & Disable DNS checking
  if (legacy) {
    smtp = simplesmtp.createServer({
      disableDNSValidation: true,
      requireAuthentication: !!(user && password),
      incomingUser: user,
      incomingPassword: password
    });

    smtp.on('startData', handleLegacyDataStream);
    smtp.on('data',      handleLegacyChunk);
    smtp.on('dataReady', handleLegacyDataStreamEnd);

    if (user && password) {
      smtp.on('authorizeUser', authorizeUser);
    }
  } else {
    smtp = new SMTPServer({
      incomingUser: user,
      incomingPassword: password,
      onAuth: authorizeUser,
      onData: handleDataStream,
      logger: false,
      disabledCommands: !!(user && password)?['STARTTLS']:['AUTH']
    });
  }

  // Setup temp folder for attachments
  createTempFolder();

  mailServer.port = port || defaultPort;
  mailServer.host = host || defaultHost;
}
```
- example usage
```shell
...
if (config.verbose) {
  logger.setLevel(2);
} else if (config.silent) {
  logger.setLevel(0);
}

// Start the Mailserver & Web GUI
mailserver.create(config.smtp, config.ip, config.incomingUser, config.incomingPass);

if (config.outgoingHost ||
    config.outgoingPort ||
    config.outgoingUser ||
    config.outgoingPass ||
    config.outgoingSecure) {
...
```

#### <a name="apidoc.element.maildev.mailserver.deleteAllEmail"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>deleteAllEmail (done)](#apidoc.element.maildev.mailserver.deleteAllEmail)
- description and source-code
```javascript
deleteAllEmail = function (done){

  logger.warn('Deleting all email');

  clearTempFolder();
  store.length = 0;
  eventEmitter.emit('delete', {id:'all'});

  done(null, true);
}
```
- example usage
```shell
...
  });

});

// Delete all emails
router.delete('/email/all', function(req, res){

  mailserver.deleteAllEmail(function(err){
    if (err) return res.status(500).json({ error: err.message });

    res.json(true);
  });

});
...
```

#### <a name="apidoc.element.maildev.mailserver.deleteEmail"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>deleteEmail (id, done)](#apidoc.element.maildev.mailserver.deleteEmail)
- description and source-code
```javascript
deleteEmail = function (id, done){
  var email      = null;
  var emailIndex = null;

  store.forEach(function(element, index){
    if (element.id === id){
      email = element;
      emailIndex = index;
    }
  });

  if (emailIndex === null){
    return done(new Error('Email not found'));
  }

  //delete raw email
  fs.unlink( path.join(tempDir, id + '.eml'), function (err) {
    if (err) {
      logger.error(err);
    } else {
      eventEmitter.emit('delete', {id:id, index:emailIndex});
    }
  });

  if (email.attachments){
    deleteAttachments(email.attachments);
  }

  logger.warn('Deleting email - %s', email.subject);

  store.splice(emailIndex, 1);

  done(null, true);
}
```
- example usage
```shell
...
  });

});

// Delete email by id
router.delete('/email/:id', function(req, res){

  mailserver.deleteEmail(req.params.id, function(err){
    if (err) return res.status(500).json({ error: err.message });

    res.json(true);
  });

});
...
```

#### <a name="apidoc.element.maildev.mailserver.emit"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>emit ()](#apidoc.element.maildev.mailserver.emit)
- description and source-code
```javascript
emit = function () { [native code] }
```
- example usage
```shell
...

  if (outgoing.isAutoRelayEnabled()) {
    mailServer.relayMail(object, true, function (err) {
      if (err) logger.error('Error when relaying email', err);
    });
  }

  eventEmitter.emit('new', object);
}

// Save an attachment
function saveAttachment(attachment){
  var output = fs.createWriteStream(path.join(tempDir, attachment.contentId));
  attachment.stream.pipe(output);
}
...
```

#### <a name="apidoc.element.maildev.mailserver.end"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>end (callback)](#apidoc.element.maildev.mailserver.end)
- description and source-code
```javascript
end = function (callback) {
  var method = legacy ? 'end' : 'close';
  smtp[method](callback);
  outgoing.close();
}
```
- example usage
```shell
...

function handleLegacyChunk(connection, chunk) {
  connection.saveStream.write(chunk);
  connection.saveRawStream.write(chunk);
}

function handleLegacyDataStreamEnd(connection, done) {
  connection.saveStream.end();
  connection.saveRawStream.end();
  // ABC is the queue id to be advertised to the client
  // There is no current significance to this.
  done(null, 'ABC');
}

function handleDataStream(stream, session, callback) {
...
```

#### <a name="apidoc.element.maildev.mailserver.getAllEmail"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>getAllEmail (done)](#apidoc.element.maildev.mailserver.getAllEmail)
- description and source-code
```javascript
getAllEmail = function (done){
  done(null, store);
}
```
- example usage
```shell
...

module.exports = function(app, mailserver, basePathname) {
var router = express.Router();

// Get all emails
router.get('/email', function(req, res){

  mailserver.getAllEmail(function(err, emailList){
    if (err) return res.status(404).json([]);

    res.json(emailList);
  });

});
...
```

#### <a name="apidoc.element.maildev.mailserver.getEmail"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>getEmail (id, done)](#apidoc.element.maildev.mailserver.getEmail)
- description and source-code
```javascript
getEmail = function (id, done){

  var email = store.filter(function(element){
    return element.id === id;
  })[0];

  if (email) {
    done(null, email);
  } else {
    done(new Error('Email was not found'));
  }
}
```
- example usage
```shell
...

/**
 * Returns a readable stream of the raw email
 */

mailServer.getRawEmail = function(id, done){

  mailServer.getEmail(id, function(err, email){
    if (err) return done(err);

    done(null, fs.createReadStream( path.join(tempDir, id + '.eml') ) );
  });
};

/**
...
```

#### <a name="apidoc.element.maildev.mailserver.getEmailAttachment"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>getEmailAttachment (id, filename, done)](#apidoc.element.maildev.mailserver.getEmailAttachment)
- description and source-code
```javascript
getEmailAttachment = function (id, filename, done){

  mailServer.getEmail(id, function(err, email){
    if (err) return done(err);

    if (!email.attachments || !email.attachments.length) {
      return done(new Error('Email has no attachments'));
    }

    var match = email.attachments.filter(function(attachment){
      return attachment.generatedFileName === filename;
    })[0];

    if (!match) {
      return done(new Error('Attachment not found'));
    }

    done(null, match.contentType, fs.createReadStream( path.join(tempDir, match.contentId) ) );

  });

}
```
- example usage
```shell
...
  });

});

// Serve Attachments
router.get('/email/:id/attachment/:filename', function(req, res){

  mailserver.getEmailAttachment(req.params.id, req.params.filename, function(err, contentType, readStream){
    if (err) return res.status(404).json('File not found');

    res.contentType(contentType);
    readStream.pipe(res);
  });

});
...
```

#### <a name="apidoc.element.maildev.mailserver.getEmailEml"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>getEmailEml (id, done)](#apidoc.element.maildev.mailserver.getEmailEml)
- description and source-code
```javascript
getEmailEml = function (id, done) {
  mailServer.getEmail(id, function(err, email){
    if (err) return done(err);

    var filename = email.id + '.eml';

    done(null, 'message/rfc822', filename, fs.createReadStream(path.join(tempDir, id + '.eml')));
  });
}
```
- example usage
```shell
...
});

  });

  // Serve email.eml
  router.get('/email/:id/download', function(req, res){

mailserver.getEmailEml(req.params.id, function(err, contentType, filename, readStream){
  if (err) return res.status(404).json('File not found');

  res.setHeader('Content-disposition', 'attachment; filename=' + filename);
  res.contentType(contentType);
  readStream.pipe(res);
});
...
```

#### <a name="apidoc.element.maildev.mailserver.getEmailHTML"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>getEmailHTML (id, baseUrl, done)](#apidoc.element.maildev.mailserver.getEmailHTML)
- description and source-code
```javascript
getEmailHTML = function (id, baseUrl, done) {

  if (!done && typeof baseUrl === 'function') {
    done = baseUrl;
    baseUrl = null;
  }

  if (baseUrl)
    baseUrl = '//' + baseUrl;

  mailServer.getEmail(id, function(err, email) {
    if (err) return done(err);

    var html = email.html;

    if (!email.attachments)
      return done(null, html);

    var embeddedAttachments = email.attachments.filter(function(attachment) {
      return attachment.contentId;
    });

    var getFileUrl = function(id, baseUrl, filename) {
      return (baseUrl || '') + '/email/' + id + '/attachment/' + filename;
    };

    if (embeddedAttachments.length) {
      embeddedAttachments.forEach(function(attachment) {
        var regex = new RegExp('src=("|\')cid:' + attachment.contentId  + '("|\')', 'g');
        var replacement = 'src="' + getFileUrl(id, baseUrl, attachment.generatedFileName) + '"';
        html = html.replace(regex, replacement);
      });
    }

    done(null, html);
  });
}
```
- example usage
```shell
...

// Get Email HTML
router.get('/email/:id/html', function(req, res){

  // Use the headers over hostname to include any port
  var baseUrl = req.headers.host + (req.baseUrl || '');

  mailserver.getEmailHTML(req.params.id, baseUrl, function(err, html){
    if (err) return res.status(404).json({ error: err.message });

    res.send(html);
  });

});
...
```

#### <a name="apidoc.element.maildev.mailserver.getOutgoingHost"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>getOutgoingHost ()](#apidoc.element.maildev.mailserver.getOutgoingHost)
- description and source-code
```javascript
getOutgoingHost = function () {
  return outgoing.getOutgoingHost();
}
```
- example usage
```shell
...
};

mailServer.isOutgoingEnabled = function() {
 return outgoing.isEnabled();
};

mailServer.getOutgoingHost = function() {
 return outgoing.getOutgoingHost();
};


/**
* Set Auto Relay Mode, automatic send email to recipient
*/
...
```

#### <a name="apidoc.element.maildev.mailserver.getRawEmail"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>getRawEmail (id, done)](#apidoc.element.maildev.mailserver.getRawEmail)
- description and source-code
```javascript
getRawEmail = function (id, done){

  mailServer.getEmail(id, function(err, email){
    if (err) return done(err);

    done(null, fs.createReadStream( path.join(tempDir, id + '.eml') ) );
  });
}
```
- example usage
```shell
...
    mailServer.relayMail(email, done);
  });
  return;
}

var mail = idOrMailObject;

mailServer.getRawEmail(mail.id, function(err, rawEmailStream) {
  if (err) {
    logger.error('Mail Stream Error: ', err);
    return done(err);
  }

  outgoing.relayMail(mail, rawEmailStream, isAutoRelay, done);
});
...
```

#### <a name="apidoc.element.maildev.mailserver.isOutgoingEnabled"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>isOutgoingEnabled ()](#apidoc.element.maildev.mailserver.isOutgoingEnabled)
- description and source-code
```javascript
isOutgoingEnabled = function () {
  return outgoing.isEnabled();
}
```
- example usage
```shell
...

// Get any config settings for display
router.get('/config', function(req, res){

  res.json({
    version:  pkg.version,
    smtpPort: mailserver.port,
    isOutgoingEnabled: mailserver.isOutgoingEnabled(),
    outgoingHost: mailserver.getOutgoingHost()
  });

});

// Relay the email
router.post('/email/:id/relay/:relayTo?', function(req, res){
...
```

#### <a name="apidoc.element.maildev.mailserver.listen"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>listen (callback)](#apidoc.element.maildev.mailserver.listen)
- description and source-code
```javascript
listen = function (callback) {

  if (typeof callback !== 'function') callback = null;

  // Listen on the specified port
  smtp.listen(mailServer.port, mailServer.host, function(err) {
    if (err) {
      if (callback) {
        callback(err);
      } else {
        throw err;
      }
    }

    if (callback) callback();

    logger.info('MailDev SMTP Server running at %s:%s', mailServer.host, mailServer.port);
  });
}
```
- example usage
```shell
...
[API docs](https://github.com/djfarrelly/MailDev/blob/master/docs/api.md).

'''javascript
var MailDev = require('maildev');

var maildev = new MailDev();

maildev.listen();

maildev.on('new', function(email){
  // We got a new email!
});
'''

MailDev also has a **REST API**. For more info
...
```

#### <a name="apidoc.element.maildev.mailserver.on"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>on ()](#apidoc.element.maildev.mailserver.on)
- description and source-code
```javascript
on = function () { [native code] }
```
- example usage
```shell
...
'''javascript
var MailDev = require('maildev');

var maildev = new MailDev();

maildev.listen();

maildev.on('new', function(email){
  // We got a new email!
});
'''

MailDev also has a **REST API**. For more info
[view the docs](https://github.com/djfarrelly/MailDev/blob/master/docs/rest.md).
...
```

#### <a name="apidoc.element.maildev.mailserver.relayMail"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>relayMail (idOrMailObject, isAutoRelay, done)](#apidoc.element.maildev.mailserver.relayMail)
- description and source-code
```javascript
relayMail = function (idOrMailObject, isAutoRelay, done) {

  if (!outgoing.isEnabled())
    return done(new Error('Outgoing mail not configured'));

  // isAutoRelay is an option argument
  if (typeof isAutoRelay === 'function') {
    done = isAutoRelay;
    isAutoRelay = false;
  }

  // If we receive a email id, get the email object
  if (typeof idOrMailObject === 'string') {
    mailServer.getEmail(idOrMailObject, function(err, email) {
      if (err) return done(err);
      mailServer.relayMail(email, done);
    });
    return;
  }

  var mail = idOrMailObject;

  mailServer.getRawEmail(mail.id, function(err, rawEmailStream) {
    if (err) {
      logger.error('Mail Stream Error: ', err);
      return done(err);
    }

    outgoing.relayMail(mail, rawEmailStream, isAutoRelay, done);
  });
}
```
- example usage
```shell
...
  object.source = path.join(tempDir, id + '.eml');

  store.push(object);

  logger.log('Saving email: ', mailObject.subject);

  if (outgoing.isAutoRelayEnabled()) {
    mailServer.relayMail(object, true, function (err) {
      if (err) logger.error('Error when relaying email', err);
    });
  }

  eventEmitter.emit('new', object);
}
...
```

#### <a name="apidoc.element.maildev.mailserver.removeAllListeners"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>removeAllListeners ()](#apidoc.element.maildev.mailserver.removeAllListeners)
- description and source-code
```javascript
removeAllListeners = function () { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.maildev.mailserver.removeListener"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>removeListener ()](#apidoc.element.maildev.mailserver.removeListener)
- description and source-code
```javascript
removeListener = function () { [native code] }
```
- example usage
```shell
...
  return function onConnection(socket) {

    // When a new email arrives, the 'new' event will be emitted
    mailserver.on('new', emitNewMail(socket));
    mailserver.on('delete', emitDeleteMail(socket));

    socket.on('disconnect', function(){
      mailserver.removeListener('new', emitNewMail(socket));
      mailserver.removeListener('delete', emitDeleteMail(socket));
    });

  };
}

/**
...
```

#### <a name="apidoc.element.maildev.mailserver.setAutoRelayMode"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>setAutoRelayMode (enabled, rules)](#apidoc.element.maildev.mailserver.setAutoRelayMode)
- description and source-code
```javascript
setAutoRelayMode = function (enabled, rules) {
  outgoing.setAutoRelayMode(enabled, rules);
}
```
- example usage
```shell
...
    config.outgoingUser,
    config.outgoingPass,
    config.outgoingSecure
  );
}

if (config.autoRelay){
  mailserver.setAutoRelayMode(true, config.autoRelayRules);
}

// Default to run on same IP as smtp
var webIp = config.webIp ? config.webIp : config.ip;
web.start(config.web, webIp, mailserver, config.webUser, config.webPass, config.basePathname);

if (config.open){
...
```

#### <a name="apidoc.element.maildev.mailserver.setupOutgoing"></a>[function <span class="apidocSignatureSpan">maildev.mailserver.</span>setupOutgoing (host, port, user, pass, secure)](#apidoc.element.maildev.mailserver.setupOutgoing)
- description and source-code
```javascript
setupOutgoing = function (host, port, user, pass, secure) {
  outgoing.setup(host, port, user, pass, secure);
}
```
- example usage
```shell
...

if (config.outgoingHost ||
    config.outgoingPort ||
    config.outgoingUser ||
    config.outgoingPass ||
    config.outgoingSecure) {

  mailserver.setupOutgoing(
    config.outgoingHost,
    parseInt(config.outgoingPort),
    config.outgoingUser,
    config.outgoingPass,
    config.outgoingSecure
  );
}
...
```



# <a name="apidoc.module.maildev.outgoing"></a>[module maildev.outgoing](#apidoc.module.maildev.outgoing)

#### <a name="apidoc.element.maildev.outgoing._createClient"></a>[function <span class="apidocSignatureSpan">maildev.outgoing.</span>_createClient ()](#apidoc.element.maildev.outgoing._createClient)
- description and source-code
```javascript
_createClient = function () {
  try {
    client = new SMTPConnection({
      port: config.port,
      host: config.host,
      secure: config.secure,
      auth: (config.pass && config.user) ?
            { user: config.user, pass: config.pass } :
            false,
      tls: { rejectUnauthorized: false },
      debug: true
    });

    logger.info(
      'MailDev outgoing SMTP Server %s:%d (user:%s, pass:%s, secure:%s)',
      config.host,
      config.port,
      config.user,
      config.pass ? '####' : config.pass,
      config.secure ? 'yes' : 'no'
    );
  } catch (err){
    logger.error('Error during configuration of SMTP Server for outgoing email', err);
  }
}
```
- example usage
```shell
...

  config.host = host;
  config.port = port;
  config.user = user;
  config.pass = pass;
  config.secure = secure;

  this._createClient();

  // Create a queue to sent out the emails
  // We use a queue so we don't run into concurrency issues
  emailQueue = async.queue(relayWorker, 1);
};

outgoing._createClient = function() {
...
```

#### <a name="apidoc.element.maildev.outgoing.close"></a>[function <span class="apidocSignatureSpan">maildev.outgoing.</span>close ()](#apidoc.element.maildev.outgoing.close)
- description and source-code
```javascript
close = function () {
  if (this.isEnabled())
    client.close();
}
```
- example usage
```shell
...
/**
* Stop the mailserver
*/

mailServer.end = function(callback) {
 var method = legacy ? 'end' : 'close';
 smtp[method](callback);
 outgoing.close();
};


/**
* Extend Event Emitter methods
* events:
*   'new' - emitted when new email has arrived
...
```

#### <a name="apidoc.element.maildev.outgoing.getOutgoingHost"></a>[function <span class="apidocSignatureSpan">maildev.outgoing.</span>getOutgoingHost ()](#apidoc.element.maildev.outgoing.getOutgoingHost)
- description and source-code
```javascript
getOutgoingHost = function () {
  return config.host;
}
```
- example usage
```shell
...
};

mailServer.isOutgoingEnabled = function() {
 return outgoing.isEnabled();
};

mailServer.getOutgoingHost = function() {
 return outgoing.getOutgoingHost();
};


/**
* Set Auto Relay Mode, automatic send email to recipient
*/
...
```

#### <a name="apidoc.element.maildev.outgoing.isAutoRelayEnabled"></a>[function <span class="apidocSignatureSpan">maildev.outgoing.</span>isAutoRelayEnabled ()](#apidoc.element.maildev.outgoing.isAutoRelayEnabled)
- description and source-code
```javascript
isAutoRelayEnabled = function () {
  return config.autoRelay;
}
```
- example usage
```shell
...
  object.envelope = envelope;
  object.source = path.join(tempDir, id + '.eml');

  store.push(object);

  logger.log('Saving email: ', mailObject.subject);

  if (outgoing.isAutoRelayEnabled()) {
    mailServer.relayMail(object, true, function (err) {
      if (err) logger.error('Error when relaying email', err);
    });
  }

  eventEmitter.emit('new', object);
}
...
```

#### <a name="apidoc.element.maildev.outgoing.isEnabled"></a>[function <span class="apidocSignatureSpan">maildev.outgoing.</span>isEnabled ()](#apidoc.element.maildev.outgoing.isEnabled)
- description and source-code
```javascript
isEnabled = function () {
  return !!client;
}
```
- example usage
```shell
...
 * Setup outgoing
 */
mailServer.setupOutgoing = function(host, port, user, pass, secure) {
  outgoing.setup(host, port, user, pass, secure);
};

mailServer.isOutgoingEnabled = function() {
  return outgoing.isEnabled();
};

mailServer.getOutgoingHost = function() {
  return outgoing.getOutgoingHost();
};
...
```

#### <a name="apidoc.element.maildev.outgoing.relayMail"></a>[function <span class="apidocSignatureSpan">maildev.outgoing.</span>relayMail (emailObject, emailStream, isAutoRelay, callback)](#apidoc.element.maildev.outgoing.relayMail)
- description and source-code
```javascript
relayMail = function (emailObject, emailStream, isAutoRelay, callback) {
  emailQueue.push({
    emailObject: emailObject,
    emailStream: emailStream,
    isAutoRelay: isAutoRelay,
    callback: callback
  });
}
```
- example usage
```shell
...
  object.source = path.join(tempDir, id + '.eml');

  store.push(object);

  logger.log('Saving email: ', mailObject.subject);

  if (outgoing.isAutoRelayEnabled()) {
    mailServer.relayMail(object, true, function (err) {
      if (err) logger.error('Error when relaying email', err);
    });
  }

  eventEmitter.emit('new', object);
}
...
```

#### <a name="apidoc.element.maildev.outgoing.setAutoRelayMode"></a>[function <span class="apidocSignatureSpan">maildev.outgoing.</span>setAutoRelayMode (enabled, rules)](#apidoc.element.maildev.outgoing.setAutoRelayMode)
- description and source-code
```javascript
setAutoRelayMode = function (enabled, rules) {

  if (!client){
    config.autoRelay = false;
    logger.info('Outgoing mail not configured - Auto relay mode ignored');
    return;
  }

  if (rules) {

    if (typeof rules === 'string') {
      try {
        rules = JSON.parse(fs.readFileSync(rules, 'utf8'));
      } catch (err) {
        logger.error('Error reading config file at ' + rules);
        throw err;
      }
    }

    if (Array.isArray(rules)) {
      config.autoRelayRules = rules;
    }
  }

  config.autoRelay = enabled;

  if (config.autoRelay) {
    logger.info(
      'Auto-Relay mode on, relay rules: %s',
      JSON.stringify(config.autoRelayRules)
    );
  }
}
```
- example usage
```shell
...
    config.outgoingUser,
    config.outgoingPass,
    config.outgoingSecure
  );
}

if (config.autoRelay){
  mailserver.setAutoRelayMode(true, config.autoRelayRules);
}

// Default to run on same IP as smtp
var webIp = config.webIp ? config.webIp : config.ip;
web.start(config.web, webIp, mailserver, config.webUser, config.webPass, config.basePathname);

if (config.open){
...
```

#### <a name="apidoc.element.maildev.outgoing.setup"></a>[function <span class="apidocSignatureSpan">maildev.outgoing.</span>setup (host, port, user, pass, secure)](#apidoc.element.maildev.outgoing.setup)
- description and source-code
```javascript
setup = function (host, port, user, pass, secure) {

  //defaults
  port = port || (secure ? 465 : 25);
  host = host || 'localhost';
  secure = secure || false;

  config.host = host;
  config.port = port;
  config.user = user;
  config.pass = pass;
  config.secure = secure;

  this._createClient();

  // Create a queue to sent out the emails
  // We use a queue so we don't run into concurrency issues
  emailQueue = async.queue(relayWorker, 1);
}
```
- example usage
```shell
...

};

/**
 * Setup outgoing
 */
mailServer.setupOutgoing = function(host, port, user, pass, secure) {
  outgoing.setup(host, port, user, pass, secure);
};

mailServer.isOutgoingEnabled = function() {
  return outgoing.isEnabled();
};

mailServer.getOutgoingHost = function() {
...
```



# <a name="apidoc.module.maildev.web"></a>[module maildev.web](#apidoc.module.maildev.web)

#### <a name="apidoc.element.maildev.web.close"></a>[function <span class="apidocSignatureSpan">maildev.web.</span>close (callback)](#apidoc.element.maildev.web.close)
- description and source-code
```javascript
close = function (callback) {
  server.close(callback);
}
```
- example usage
```shell
...
/**
* Stop the mailserver
*/

mailServer.end = function(callback) {
 var method = legacy ? 'end' : 'close';
 smtp[method](callback);
 outgoing.close();
};


/**
* Extend Event Emitter methods
* events:
*   'new' - emitted when new email has arrived
...
```

#### <a name="apidoc.element.maildev.web.start"></a>[function <span class="apidocSignatureSpan">maildev.web.</span>start (port, host, mailserver, user, password, basePathname)](#apidoc.element.maildev.web.start)
- description and source-code
```javascript
start = function (port, host, mailserver, user, password, basePathname) {

  if (user && password) {
    app.use(auth(user, password));
  }

  if (basePathname) {
    io.path(basePathname + '/socket.io');
  } else {
    basePathname = '/';
  }

  app.use(basePathname, express.static(path.join(__dirname, '../app')));

  routes(app, mailserver, basePathname);

  io.attach(server);
  io.on('connection', webSocketConnection(mailserver));

  port = port || 1080;
  host = host || '0.0.0.0';

  server.listen(port, host);

  logger.info('MailDev app running at %s:%s', host, port);

}
```
- example usage
```shell
...

if (config.autoRelay){
  mailserver.setAutoRelayMode(true, config.autoRelayRules);
}

// Default to run on same IP as smtp
var webIp = config.webIp ? config.webIp : config.ip;
web.start(config.web, webIp, mailserver, config.webUser, config.webPass, config.basePathname);

if (config.open){
  var open = require('open');
  open('http://' + (config.ip === '0.0.0.0' ? 'localhost' : config.ip) + ':' + config.web);
}

process.on('SIGTERM', function () {
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
