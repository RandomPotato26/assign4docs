
# API

a guide to our provided JS library for the people out there who want to use our technology outside of our app

## Getting Started

*****

### install Fact Checker
    npm install FactChecker

verify Fact Checker version
``` JavaScript
    npm FactChecker -v
```

!!! warning
    update FactChecker to the latest version before continuing

    **latest version is `2.4`** 


import JavaScript library into your project and connect to the database

    var facts = require(`FactChecker`);

    facts.connect('NA', JWT)

optional strings for server connections `.connect( server )` : : `EU`, `NA`, `CN`

provide a JWT (learn more at https://jwt.io/)

*****

## Example Overview
using ES6 Promise and a proprietary photo capture library 

    var facts = require(`FactChecker`);
    var photo = require('JasonCam')
    facts.connect('NA', exampleJWT);

    var isFact = new Promise(function(){ 
        return facts.checkPhoto(JasonCam.capturePhoneCamera(), {OCR_Model: JasonCam.JasonRecog})
    );

    isFact.resolve(console.log)
    //returns wether or not the person looking at the Jason's Phone is Jason

*****


## Methods

all methods return a true/false value or an error

!!!info
    our API supports offline and third-party OCRs the default OCR for all methods  `https://widgits.inc/PublicOCR.model`


### audio file

    facts.checkAudio(myAudioFile , OPTIONS);

*****

### video file

acceptable video formats include `.mov`, `.mp4`, and `.webem`

    facts.checkVideo(myVidoFile , OPTIONS);

!!!info
    `OPTIONS` is read as a standard JS object, potential values are 

        OPTIONS{
            OCR_Model: ./path/to/myOCRModel OR https://exampleOCR.com/myOCRmodel.model,
            checkAudio: true/false, 
            checkVisual: true/false, 
        }

### photo file

acceptable photo formats include `.png`, `.jpg`, and `.svg`

    facts.checkPhoto(myPhoto, OPTIONS)

### document file

acceptable document formats include `.pdf`, `.doc`, `.docx`, `.txt`, and `.rtf`

    facts.checkDocument(myDocument, OPTIONS)

!!!warning
    OCR for PDFs can be sketchy at times


*****

## Advanced
### Streams

Audio Stream

```JavaScript
var audioStream = new facts.audioStream(myAudioStream);
facts.checkAudioStream(audioStream);
```

Video Stream

```JavaScript
var videoStream = new facts.videoStream(myVideoStream);
facts.checkVidoStream(videoStream);
```